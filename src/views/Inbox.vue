<template>
  <b-container class="inbox-view">
    <b-row align-h="center">
      <b-col lg="8">
        <b-form-input
          class="border rounded-pill shadow"
          style="border-color: #f5f5f5"
          v-model="searchText"
          placeholder="Buscar chat"
        ></b-form-input>
      </b-col>
    </b-row>

    <b-row align-h="center" class="chat-group">
      <b-col cols="12" lg="8">
        <b-list-group class="mt-5 shadow">
          <b-list-group-item to="/chat" class="d-flex">
            <b-avatar
              badge
              badge-variant="success"
              :src="userAvatar"
            ></b-avatar>
            <div class="chat-list-body">
              <span class="chat-name">Luis Suarez Martinez</span>
              <span class="chat-preview">Lorem Ipsum Dolor sit amet.</span>
            </div>
            <div class="chat-time">
              <span class="chat-time-text">Now</span>
              <b-badge>2</b-badge>
            </div>
          </b-list-group-item>
          <b-list-group-item to="/chat" class="d-flex">
            <b-avatar
              badge
              badge-variant="success"
              :src="userAvatar"
            ></b-avatar>
            <div class="chat-list-body">
              <span class="chat-name">Carlos Olivares</span>
              <span class="chat-preview">Lorem Ipsum Dolor sit amet.</span>
            </div>
            <div class="chat-time">
              <span class="chat-time-text">12:00</span>
            </div>
          </b-list-group-item>
          <b-list-group-item to="/chat" class="d-flex">
            <b-avatar
              :src="userAvatar"
            ></b-avatar>
            <div class="chat-list-body">
              <span class="chat-name">Mariana Sanchez</span>
              <span class="chat-preview">Lorem Ipsum Dolor sit amet.</span>
            </div>
            <div class="chat-time">
              <span class="chat-time-text">12:00</span>
              <b-badge>2</b-badge>
            </div>
          </b-list-group-item>
          <b-list-group-item to="/chat" class="d-flex">
            <b-avatar
              badge
              badge-variant="success"
              :src="userAvatar"
            ></b-avatar>
            <div class="chat-list-body">
              <span class="chat-name">Paola Gonzalez</span>
              <span class="chat-preview">Lorem Ipsum Dolor sit amet.</span>
            </div>
            <div class="chat-time">
              <span class="chat-time-text">12:00</span>
            </div>
          </b-list-group-item>
          <b-list-group-item to="/chat" class="d-flex">
            <b-avatar

              :src="userAvatar"
            ></b-avatar>
            <div class="chat-list-body">
              <span class="chat-name">Roberto Salinas</span>
              <span class="chat-preview">Lorem Ipsum Dolor sit amet.</span>
            </div>
            <div class="chat-time">
              <span class="chat-time-text">12:00</span>
            </div>
          </b-list-group-item>
          <b-list-group-item to="/chat" class="d-flex">
            <b-avatar

              :src="userAvatar"
            ></b-avatar>
            <div class="chat-list-body">
              <span class="chat-name">Pablo Rivera</span>
              <span class="chat-preview">Lorem Ipsum Dolor sit amet.</span>
            </div>
            <div class="chat-time">
              <span class="chat-time-text">12:00</span>
            </div>
          </b-list-group-item>
        </b-list-group>
      </b-col>
    </b-row>
    <Footer />
  </b-container>
</template>

<script>
// @ is an alias to /src
import Footer from "@/components/Footer.vue";

export default {
  name: "Inbox",
  components: {
    Footer,
  },
  data() {
    return {
      searchText: "",
      userAvatar: require("../assets/img/user@4x.webp"),
    };
  },
};
</script>

<style lang="scss">
.inbox-view {
  padding-top: 98px;
  input {
    font-family: "Montserrat", sans-serif;
  }
  .chat-group {
    .col-12 {
      .list-group {
        border-radius: 15px;
        .b-avatar {
          margin-right: 15px;
          .b-avatar-badge {
            min-height: 1.2em;
            min-width: 1.2em;
            &.badge-success {
              background: #33c410;
            }
          }
        }
        .chat-list-body {
          flex: 1 1 0;
          .chat-name {
            color: #1d1d1d;
            font-family: "Montserrat", sans-serif;
            font-size: 14px;
            font-weight: bold;
            display: block;
            text-align: left;
          }
          .chat-preview {
            color: #858687;
            font-family: "Montserrat", sans-serif;
            font-size: 12px;
            display: block;
            text-align: left;
          }
        }
        .chat-time {
          align-items: flex-start;
          .chat-time-text {
            font-family: "Montserrat", sans-serif;
            font-size: 11px;
            display: block;
          }
          .badge {
            background: #d4ebdf;
            color: #33c422;
            border-radius: 100%;
          }
        }
      }
    }
  }
}
</style>
