<template>
  <b-container class="chat-view">
    <b-row class="chat-group">
      <b-col cols="12">
        <b-list-group>
          <b-list-group-item
            class="d-flex align-items-center justify-content-center border-0"
          >
            <router-link to="/inbox"
              ><p class="h1 mb-0" style="margin-right: 15px">
                <b-icon style="color: black" icon="arrow-left"></b-icon></p
            ></router-link>

            <b-avatar
              badge
              badge-variant="success"
              :src="userAvatar"
            ></b-avatar>
            <div class="chat-list-body">
              <span class="chat-name">Luis Suarez Martinez</span>
              <span class="chat-preview">Lorem Ipsum Dolor sit amet.</span>
            </div>
          </b-list-group-item>
        </b-list-group>
      </b-col>
    </b-row>

    <b-row class="chat-container">
      <b-col cols="12">
        <div class="messages">
          <ul class="pl-0">
            <li class="sent">
              <b-avatar size="1.6rem" :src="userAvatar"></b-avatar>
              <p>
                How the hell am I supposed to get a jury to believe you when I
                am not even sure that I do?!
              </p>
            </li>
            <li class="replies">
              <b-avatar size="1.6rem" :src="userAvatar"></b-avatar>
              <p>
                When you're backed against the wall, break the god damn thing
                down.
              </p>
            </li>
            <li class="replies">
              <b-avatar size="1.6rem" :src="userAvatar"></b-avatar>
              <p>Excuses don't win championships.</p>
            </li>
            <li class="sent">
              <b-avatar size="1.6rem" :src="userAvatar"></b-avatar>
              <p>Oh yeah, did Michael Jordan tell you that?</p>
            </li>
            <li class="replies">
              <b-avatar size="1.6rem" :src="userAvatar"></b-avatar>
              <p>No, I told him that.</p>
            </li>
            <li class="replies">
              <b-avatar size="1.6rem" :src="userAvatar"></b-avatar>
              <p>What are your choices when someone puts a gun to your head?</p>
            </li>
            <li class="sent">
              <b-avatar size="1.6rem" :src="userAvatar"></b-avatar>
              <p>
                What are you talking about? You do what they say or they shoot
                you.
              </p>
            </li>
            <li class="replies">
              <b-avatar size="1.6rem" :src="userAvatar"></b-avatar>
              <p>
                Wrong. You take the gun, or you pull out a bigger one. Or, you
                call their bluff. Or, you do any one of a hundred and forty six
                other things.
              </p>
            </li>
          </ul>
        </div>
      </b-col>
    </b-row>
    <b-row class="chat-input">
      <b-col>
        <b-input-group
          class="border rounded-pill shadow"
          style="border-color: #f5f5f5"
        >
          <b-form-input
            class="border-0 rounded-pill shadow-none"
            v-model="searchText"
            placeholder="Mensaje..."
          ></b-form-input>
          <b-input-group-append>
            <p class="h2 mb-0" style="margin-right: 15px">
              <b-icon style="color: black" icon="paperclip"></b-icon>
            </p>
          </b-input-group-append>
        </b-input-group>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
export default {
  name: "Chat",
  data() {
    return {
      searchText: "",
      userAvatar: require("../assets/img/user@4x.webp"),
    };
  },
};
</script>

<style lang="scss">
.chat-view {
  padding-top: 60px;
  .chat-input {
    position: fixed;
    bottom: 0;
    width: 100%;
    padding-bottom: 25px;
    background: white;
    .col {
      .input-group {
        align-items: center;
        input {
          font-family: "Montserrat", sans-serif;
        }
        .input-group-append {
          svg {
            transform: rotate(30deg);
          }
        }
      }
    }
  }
  .chat-group {
    box-shadow: 0px 10px 10px -6px rgba(0, 0, 0, 0.5);
    background: white;
    padding-bottom: 7px;
    padding-top: 7px;
    position: -webkit-sticky;
    position: sticky;
    top: 0px;
    z-index: 1;
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
  .chat-container {
    overflow: hidden;
    .messages {
      height: auto;
      min-height: calc(100% - 93px);
      max-height: calc(100% - 93px);
      //overflow-y: scroll;
      //overflow-x: hidden;
      ul {
        &.pl-0 {
          padding-left: 0;
        }
        li {
          display: inline-block;
          margin: 15px 0 5px;
          width: 100%;
          font-size: 0.9em;
          text-align: left;
          &:nth-last-child(1) {
            margin-bottom: 20px;
          }
          &.sent {
            float: none;
            display: flex;
            //align-items: baseline;
            p {
              background: #1d1d1d;
              color: #f5f5f5;
              margin-left: 10px;
            }
          }
          &.replies {
            display: flex;
            //align-items: baseline;
            justify-content: flex-start;
            flex-direction: row-reverse;
            img {
              float: right;
              //margin: 6px 0 0 8px;
            }
            p {
              background: #f5f5f5;
              float: right;
              margin-right: 10px;
            }
          }
          img {
            //width: 22px;
            //border-radius: 50%;
            float: left;
          }
          p {
            display: inline-block;
            padding: 10px 15px;
            border-radius: 20px;
            max-width: 205px;
            line-height: 130%;
          }
        }
      }
    }
  }
}
</style>
