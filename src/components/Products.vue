<template>
  <div class="main-products">
    <div class="products-header">
      <h6>{{ searchProducts.length }} results found</h6>
      <div class="featured-btn">
        <button class="featured" @click="show">
          <h1>{{ productValue }}</h1>
          <i class="fa-solid arrw fa-angle-down"></i>
          <ul id="ftdList" class="star-menu ftd display">
            <li class="hov ftd-item" @click="def">
              <span>Featured</span>
            </li>
            <li class="hov ftd-item" @click="lowest">
              <span>Lowest</span>
            </li>
            <li class="hov ftd-item" @click="highest">
              <span>Highest</span>
            </li>
          </ul>
        </button>
        <button class="grid-icn"><i class="fa-solid fa-border-all"></i></button>
        <button class="list-icn"><i class="fa-solid fa-list"></i></button>
      </div>
    </div>

    <div class="Search-Input">
      <input v-model="searchInput" type="search" placeholder="search product" />
      <i class="fa-solid lens fa-magnifying-glass"></i>
    </div>

    <div class="all-products">
      <div v-for="item in productItems" :key="item.id" class="cards">
        <div class="card-img">
          <img :src="item.img" alt="" />
        </div>
        <div class="card-body">
          <div class="card-wrapper">
            <div class="card-ratting">
              <ul class="stars-ratting">
                <li><i class="icon fa-regular fa-star"></i></li>
                <li><i class="icon fa-regular fa-star"></i></li>
                <li><i class="icon fa-regular fa-star"></i></li>
                <li><i class="icon fa-regular fa-star"></i></li>
                <li><i class="icon fa-regular fa-star"></i></li>
              </ul>
            </div>
            <div class="item-price">
              <h6>{{ item.price }}</h6>
            </div>
          </div>
          <a class="item-name" href="#"
            ><h6>{{ item.name }}</h6></a
          >
          <p class="item-desc">
            {{ item.discription }}
          </p>
        </div>
        <div class="card-options">
          <a class="wish-icn" href=""
            ><i class="icon fa-regular fa-heart"></i>Wishlist</a
          >
          <a class="cart-icn" href=""
            ><i class="icon fa-solid fa-cart-shopping"></i>View In Cart</a
          >
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["items", "inputData"],
  data() {
    return {
      searchInput: "",
      sInput: "",
      productItems: this.items,
      productValue: "",
    };
  },
  computed: {
    searchProducts() {
      this.sInput =
        this.searchInput.charAt(0).toUpperCase() + this.searchInput.slice(1);
      this.productItems = this.items.filter((item) =>
        item.name.includes(this.sInput)
      );
      this.productItems = this.productItems.filter((item) =>
        item.brand.includes(this.inputData)
      );
      console.log(this.items.brand);
      this.productValue = "Featured";
      return this.productItems;
    },
    lowest() {
      this.productItems = this.productItems.sort((a, b) => a.price - b.price);
      this.productValue = "Lowest";
      return this.productItems;
    },
    highest() {
      this.productItems = this.productItems.sort((a, b) => b.price - a.price);
      this.productValue = "Highest";
      return this.productItems;
    },
    def() {
      this.productItems = this.items.filter((item) =>
        item.name.includes(this.sInput)
      );
      this.productValue = "Featured";
      return this.productItems;
    },
  },
  methods: {
    show: function (event) {
      document.getElementById("ftdList").classList.toggle("display");
    },
  },
};
</script>
<style>
.all-products {
  width: 915.2px;
  margin-top: 28px;
  display: flex;
  flex-flow: wrap;
}
.ftd {
  width: 138px;
  height: 115.5px;
  margin: 0;
  padding: 7px 0;
  top: 44px;
  left: -19px;
  z-index: 111;
}
.ftd .ftd-item {
  display: flex;
  font-family: Montserrat, Helvetica, Arial, serif;
  width: 102.2px;
  height: 20.3px;
  padding: 9.1px 17.92px;
  font-weight: 400;
  color: #6e6b7be8;
  white-space: nowrap;
  font-size: 14px;
  justify-content: flex-start;
}
.cards {
  min-width: 286.4px;
  height: 366px;
  margin: 0 9px;
  margin-bottom: 28px;
  overflow: hidden;
  box-shadow: 0 4px 24px 0 rgb(34 41 47 / 10%);
  background-color: #fff;
  border-radius: 0.428rem;
  flex-direction: column;
  word-wrap: break-word;
  display: flex;
  transition: 0.3s ease-in-out;
}
.cards:hover {
  transform: translateY(-5px);
  box-shadow: 0 4px 25px 0 rgb(34 41 47 / 25%);
}
.card-img {
  align-items: center;
  width: 286.4px;
  height: 214.56px;
  padding-top: 7px;
}
.card-img img {
  width: 100%;
  height: 100%;
}
.card-body {
  box-sizing: border-box;
  width: 286.4px;
  height: 104.5px;
  padding: 14px;
  letter-spacing: 0.14px;
  line-height: 20.3px;
  font-weight: 400;
  font-size: 14px;
}

.card-wrapper {
  width: 258.4px;
  height: 25.4px;
  display: flex;
  justify-content: space-between;
  margin: 0px;
}

.card-ratting {
  width: 94px;
  height: 20.3px;
  font-size: 14px;
}
.stars-ratting {
  list-style: none;
  display: flex;
  font-size: 14px;
  margin: 0px;
  padding: 0px;
}
.stars-ratting .icon {
  font-size: 14px;
  width: 16px;
  height: 16px;
  padding: 0px;
}

.item-price h6 {
  padding: 0px;
  margin: 0px;
  font-size: 14px;
  font-family: inherit;
  line-height: 1.2;
  font-weight: 600;
}
.item-name {
  text-decoration: none;
  width: 258.4px;
  height: 16.8px;
}
.item-name h6 {
  margin: 0px;
  text-decoration: none;
  color: #6e6b7b;
  font-size: 14px;
  font-weight: 600;
  line-height: 1.2;
  font-family: inherit;
  margin-top: 10px;
  letter-spacing: 0.4px;
}
.item-desc {
  box-sizing: border-box;
  width: 258.4px;
  height: 21px;
  margin-top: 2.8px;
  font-size: 12.25px;
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
  color: #6e6b7b;
}
.card-options {
  width: 286.42px;
  height: 39.6px;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  cursor: pointer;
}

.card-options .wish-icn {
  box-sizing: border-box;
  display: flex;
  width: 126.93px;
  height: 40px;
  text-align: center;
  text-decoration: none;
  padding: 0.786rem 1.5rem;
  letter-spacing: 0.4px;
  color: #2a2e30;
  font-size: 14px;
  line-height: 1;
  background-color: #f6f6f6;
}
.card-options .wish-icn:hover {
  background-color: #e3e3e3;
}
.card-options .icon {
  width: 14px;
  height: 14px;
  margin-right: 7px;
  padding: 0px;
}

.card-options .cart-icn {
  box-sizing: border-box;
  width: 159.49px;
  text-align: center;
  text-decoration: none;
  padding: 0.786rem 1.5rem;
  letter-spacing: 0.4px;
  color: #2a2e30;
  font-size: 14px;
  line-height: 1;
  background-color: #7367f0;
  color: #ffff;
}
.card-options .cart-icn:hover {
  box-shadow: 0 8px 25px -8px #7367f0;
}
.main-products {
  position: absolute;
  width: 915.2px;
  height: 1356.2px;
  margin-left: 576px;
  float: right;
  margin-top: 172.9px;
  padding-right: 28px;
}
.products-header {
  display: flex;
  height: 20px;
  align-items: center;
  justify-content: space-between;
}
.products-header h6 {
  margin: 0;
  font-size: 14px;
  font-weight: 500;
  letter-spacing: 0.8px;
}
.featured-btn {
  justify-content: flex-end;
  align-items: flex-end;
}
.featured-btn .featured {
  position: relative;
  background-color: #f8f8f8;
  padding: 11px 16px;
  border: 1px solid rgb(115, 103, 240);
  border-radius: 5px;
  cursor: pointer;
  width: 123px;
  height: 38px;
}
.arrw {
  color: #7367f0;
  padding-left: 10px;
}
.featured-btn button h1 {
  color: #7367f0;
  font-size: 14px;
  line-height: 1;
  font-weight: 500;
  letter-spacing: 0.7px;
  margin: 0;
  padding: 0;
  display: inline;
}

.featured-btn .featured:hover {
  background-color: rgba(115, 103, 240, 0.04);
}
.featured {
  margin-right: 14px;
}
.grid-icn,
.list-icn {
  width: 47px;
  height: 38px;
  padding: 6.8px 14px;
  color: #7367f0;
  background-color: #f8f8f8;
  border: 1px solid rgb(115, 103, 240);
  cursor: pointer;
  font-size: 15px;
}
.grid-icn {
  border-top-left-radius: 5px;
  border-bottom-left-radius: 5px;
  background-color: #7367f033;
}
.list-icn {
  border-top-right-radius: 5px;
  border-bottom-right-radius: 5px;
}
.list-icn:hover {
  background-color: rgba(115, 103, 240, 0.04);
}
.Search-Input {
  display: flex;
  padding-top: 6.132px;
  align-items: center;
  justify-content: space-between;
  width: 100%;
  margin-top: 22px;
  background-color: rgb(255, 255, 255);
  height: 48px;
  border-radius: 5px;
  box-shadow: 0 2px 8px 0 rgb(34 41 47 / 14%);
}

.Search-Input input {
  width: 90%;
  height: 40px;
  color: #6e6b7b;
  padding: 0px 0px 6.132px 17.5px;
  border: none;
}
.lens {
  margin-right: 15px;
}
::-webkit-input-placeholder {
  color: #b9b9c3;
}
</style>
