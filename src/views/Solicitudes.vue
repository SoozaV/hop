<template>
  <b-container class="solicitudes-view">
    <b-row align-h="center" class="view-title">
      <b-col lg="8" class="col">
        <h2>Comparte experiencias</h2>
        <h3>
          Consulta el estado de tu solicitud y reserva el número de horas ó días
          de acuerdo a tus necesidades.
        </h3>
      </b-col>
    </b-row>

    <b-row align-h="center" class="solicitudes-group">
      <b-col cols="12" lg="8">
        <b-list-group class="mt-3 shadow">
          <b-list-group-item to="/chat" class="d-flex">
            <b-avatar
              badge
              badge-variant="success"
              :src="userAvatar"
            ></b-avatar>
            <div class="solicitudes-list-body">
              <span class="status-name">Best Place Co-working</span>
              <span class="direction">Dirección # 123 Col. Reforma</span>
              <span class="status">Status: {{ status.aprobada ? "Aprobada" : "Denegada" }}</span>
            </div>
            <div class="status-time">
              <span class="status-time-text">Dic 23</span>
              <!--b-badge>2</b-badge-->
            </div>
          </b-list-group-item>
          <b-list-group-item class="d-flex">
            <b-avatar
              badge
              badge-variant="success"
              :src="userAvatar"
            ></b-avatar>
            <div class="solicitudes-list-body">
              <span class="status-name">Awesome CW</span>
              <span class="direction">Dirección # 123 Col. Doctores</span>
              <span class="status">Status: {{ status.aprobada ? "Aprobada" : "Denegada" }}</span>
            </div>
            <div class="status-time">
              <span class="status-time-text">Nov 2</span>
            </div>
          </b-list-group-item>
          <b-list-group-item class="d-flex">
            <b-avatar badge badge-variant="danger" :src="userAvatar"></b-avatar>
            <div class="solicitudes-list-body">
              <span class="status-name">Nice Place</span>
              <span class="direction">Dirección # 123 Col. Narvarte</span>
              <span class="status">Status: {{ !status.aprobada ? "Aprobada" : "Denegada" }}</span>
            </div>
            <div class="status-time">
              <span class="status-time-text">Oct 14</span>
            </div>
          </b-list-group-item>
          <b-list-group-item class="d-flex">
            <b-avatar
              badge
              badge-variant="success"
              :src="userAvatar"
            ></b-avatar>
            <div class="solicitudes-list-body">
              <span class="status-name">Just Coffee</span>
              <span class="direction">Dirección # 123 Col. Roma</span>
              <span class="status">Status: {{ status.aprobada ? "Aprobada" : "Denegada" }}</span>
            </div>
            <div class="status-time">
              <span class="status-time-text">Sep 2</span>
            </div>
          </b-list-group-item>
          <b-list-group-item class="d-flex">
            <b-avatar badge badge-variant="danger" :src="userAvatar"></b-avatar>
            <div class="solicitudes-list-body">
              <span class="status-name">Networking Studio</span>
              <span class="direction">Dirección # 123 Col. Juarez</span>
              <span class="status">Status: {{ !status.aprobada ? "Aprobada" : "Denegada" }}</span>
            </div>
            <div class="status-time">
              <span class="status-time-text">Ago 4</span>
            </div>
          </b-list-group-item>
          <b-list-group-item class="d-flex">
            <b-avatar
              badge
              badge-variant="success"
              :src="userAvatar"
            ></b-avatar>
            <div class="solicitudes-list-body">
              <span class="status-name">Best Place Co-working</span>
              <span class="direction">Dirección # 123 Col. Polanco</span>
              <span class="status">Status: {{ status.aprobada ? "Aprobada" : "Denegada" }}</span>
            </div>
            <div class="status-time">
              <span class="status-time-text">Jul 5</span>
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
  name: "Solicitudes",
  components: {
    Footer,
  },
  data() {
    return {
      searchText: "",
      userAvatar: require("../assets/img/solicitudes@3x.png"),
      status: {
        aprobada: true,
        denegada: false,
      },
    };
  },
};
</script>

<style lang="scss">
.solicitudes-view {
  padding-top: 98px;

  .view-title {
    padding-left: 18px;
    padding-right: 18px;
    .col {
      h2,
      h3 {
        text-align: left;
        font-family: "Montserrat", sans-serif;
        color: #1d1d1d;
        font-weight: 800;
        font-size: 20px;
      }
      h3 {
        font-size: 12px;
        font-weight: 400;
        line-height: 1.4em;
      }
    }
  }
  input {
    font-family: "Montserrat", sans-serif;
  }
  .solicitudes-group {
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
            &.badge-danger {
              background: #ff0000;
            }
          }
        }
        .solicitudes-list-body {
          flex: 1 1 0;
          .status-name {
            color: #1d1d1d;
            font-family: "Montserrat", sans-serif;
            font-size: 14px;
            font-weight: bold;
            display: block;
            text-align: left;
          }
          .direction, .status {
            color: #858687;
            font-family: "Montserrat", sans-serif;
            font-size: 12px;
            display: block;
            text-align: left;
          }
        }
        .status-time {
          align-items: flex-start;
          .status-time-text {
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
