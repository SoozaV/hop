<template>
  <b-row class="property-container" :style="{ 'background-color': bgColor }">
    <b-col cols="5">
      <b-img :src="propertyImage" fluid-grow alt=""></b-img>
    </b-col>
    <b-col>
      <b-col class="rank-col">
        <div class="rank">3.0</div>
        <div class="stars">
          <b-rating />
        </div>
      </b-col>
      <h2>Grat<br />Co-Working</h2>
      <div class="separador"></div>
      <h3>Example Address #77</h3>
      <b-row class="bottom-columns inner">
        <b-col cols="5"
          ><p class="price"><span class="symbol">$</span> 1430/ mens</p></b-col
        >
        <b-col
          ><p class="price">
            Book <b-button class="shadow-none border-0"></b-button></p
        ></b-col>
      </b-row>
    </b-col>
    <b-row class="bottom-columns outer">
      <b-col cols="5"
        ><p class="price"><span class="symbol">$</span> 1430/ mens</p></b-col
      >
      <b-col
        ><p class="price">
          Book <b-button class="shadow-none border-0"></b-button></p
      ></b-col>
    </b-row>
  </b-row>
</template>

<script>
export default {
  name: "Property",
  props: {
    bgColor: String,
  },
  data() {
    return {
      propertyImage: require("../assets/img/property@4x.webp"),
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
.property-container {
  padding-top: 29px;
  padding-bottom: 6px;
  font-family: "Montserrat", sans-serif;
  color: #1d1d1d;
  p.price {
    font-weight: bold;
    span.symbol {
      color: #fcca2e;
    }
    button {
      background: #fcca2e;
      width: 63px;
      height: 63px;
      border-radius: 100%;
      margin-left: 10px;
      position: relative;
      &:before {
        content: "✕";
        color: #707070;
        position: absolute;
        top: 14px;
        left: 21px;
        transform: rotate(45deg);
        font-size: 25px;
      }
    }
  }
  .separador {
    background: #1d1d1d;
    width: 32px;
    height: 3px;
    margin-bottom: 16px;
  }
  .rank-col {
    display: flex;
    justify-content: space-between;
    margin-bottom: 12px;
    .rank {
      font-weight: bold;
      font-size: 12px;
    }
    .stars {
      display: flex;
      .b-rating {
        display: block;
        padding: 0;
        background: transparent;
        border: 0;
      }
      img {
        width: 15px;
        height: 15px;
      }
    }
  }
  .bottom-columns {
    padding-top: 25px;
    div {
      display: flex;
      align-items: center;
      justify-content: center;
      &:last-child {
        justify-content: flex-end;
      }
    }
  }
}
@media screen and (max-width: 768px) {
  .property-container {
    .bottom-columns {
      &.inner {
        display: none;
      }
      &.outer {
        display: flex;
      }
    }
  }
}
@media screen and (min-width: 768px) {
  .property-container {
    padding-top: 50px;
    padding-bottom: 50px;
    .rank-col {
      .rank {
        font-size: 20px;
      }
    }
    h2 {
      font-size: 42px!important;
    }
    h3 {
      font-size: 20px!important;
    }
    .bottom-columns {
      &.inner {
        display: flex;
        & > div:first-child {
          justify-content: flex-start;
        }
      }
      &.outer {
        display: none;
      }
    }
  }
}
</style>
