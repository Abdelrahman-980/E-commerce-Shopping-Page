<template>
  <div>
    <div class="nav">
      <div class="nav-content">
        <div class="navbar-left">
          <ul class="icons-left icons">
            <li><i class="icon fa-regular fa-calendar"></i></li>
            <li><i class="icon fa-regular fa-message"></i></li>
            <li><i class="icon fa-regular fa-envelope"></i></li>
            <li><i class="icon fa-regular fa-calendar-check"></i></li>
            <li class="star" @click="show">
              <i class="icon fa-regular fa-star"></i>
              <ul id="starList" class="star-menu display">
                <li class="star-search">
                  <input type="search" placeholder="Explore Vuexy..." />
                </li>
                <li class="hov">
                  <i class="icon star-icon fa-regular fa-message"></i
                  ><span>Chat</span
                  ><i class="icon list-icon fa-regular fa-star"></i>
                </li>
                <li class="hov">
                  <i class="icon star-icon fa-regular fa-calendar"></i
                  ><span>Calendar App</span
                  ><i class="icon list-icon fa-regular fa-star"></i>
                </li>
                <li class="hov">
                  <i class="icon star-icon fa-regular fa-envelope"></i
                  ><span>Email</span
                  ><i class="icon list-icon fa-regular fa-star"></i>
                </li>
                <li class="hov">
                  <i class="icon star-icon fa-regular fa-calendar-check"></i
                  ><span>Todo</span
                  ><i class="icon list-icon fa-regular fa-star"></i>
                </li>
              </ul>
            </li>
          </ul>
        </div>
        <div class="navbar-right">
          <ul class="icons-right icons">
            <li>
              <img
                class="imggg"
                src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAGQAAAA1CAMAAACA7r40AAAA/FBMVEWyIjNPN2Y8O27///8/PnBOTXxycpY9PG9RUX5HR3dIR3dLSnlPTny4uMpWVYFFRHVwb5VlZIx7e52DgqOIh6aIiKc+PXBJSHhTUn9hYYqyIjReXohgX4lYV4Lr6/C2tcjPdYB0c5haWYRYV4Nra5GJiac+PW/FxdTHYG1RUH3eoajltbtOTXvty89BQHHg3+hSUX6GYoC6usyVlbFycZa7u8yUk6+sq8FCQXO0tMe1tMhiYYpMS3pDQnNvbpTExNN8fJ7GxdTGxtWCgqLHx9WXlrLXi5SYl7Kiobrg4Oiiorrn5u3n5+2jo7ukpLvw8PTx8fX09Pf19firqsC5sMNxAAAAAnRSTlPQ9qN1Xw4AAAGlSURBVHhe7ZXFiiRBFEVjznvp5W7t7j3u7m7//y8D1dAMGbnI4jW5KOpsgjibCxFcrrtVEmcBGAGQJHB98d3EgEM/ygsg/nwRAy15rxQ4Ywh3JQX49hVgKA/Ad1hDkkGTMSQJjGkOEmo133FmwAEQyl8FfSj3gFgkzjsQAw6AZ796AP2fGcDBS8/ZQ7ZQlJ2d+bEFqp6zhuh9Cf9/pDtKkTs04KBTD4jgx3eICOodoshz1p7M6UUAUQ+Ap2Pf2UMI5UBBX18/Ut7ZQ84Jui10QKsbcA7dt77jxIBDt+sxMNzrD4HL+rZS4Iw9iTZkCjRFmsBUHkcUOGMI7dkpKezuQsrprM3zR76zN572ekdBX623gaONJ0d5B5sGHAA1+QTwRQJgX2Q/7+w9GZGlDZKERpoxgkbDc8s0WscGSo+WGMiNVlgwWuFNjdafPsDe7wzg3RvP2UNCFGVtbX6EoOo7PhgoO1rGnswHiquB4mqgfIcxpBTGkNslMf2JVMAShRxXgJtUwBKFbFbAqicL4U4qYNWThXCHFbDqyUK4swpY9WQhXBX8A2rVjaQ6HWXmAAAAAElFTkSuQmCC"
                alt="en"
                width="22"
                height="14"
              />
            </li>
            <li><span class="span eng">English</span></li>
            <li><i class="icon fa-regular fa-moon"></i></li>
            <li><i class="icon fa-solid fa-magnifying-glass"></i></li>
            <li class="cart"><i class="icon fa-solid fa-cart-shopping"></i></li>
            <li class="notification">
              <i class="icon fa-regular fa-bell"></i>
            </li>
            <li class="john">
              <span class="span doe">John Doe</span
              ><span class="span admin">admin</span>
            </li>
            <li class="account">
              <span class="imgg"
                ><img
                  class="imggg"
                  src="https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/13-small.d796bffd.png"
              /></span>
            </li>
          </ul>
        </div>
      </div>
    </div>
    <div class="shop-container">
      <div class="shop">
        <h2>Shop</h2>
        <ul class="shop-icons">
          <li><i class="fa-solid house fa-house"></i></li>
          <li><i class="fa-solid fa-angle-right"></i></li>
          <li class="ec">ECommerce</li>
          <li class="arr2"><i class="fa-solid fa-angle-right"></i></li>
          <li class="sh">Shop</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
methods : {
        show : function (){
            document.getElementById("starList").classList.toggle("display")
        }
    }
};
</script>

<style>
.nav {
  position: fixed;
  direction: ltr;
  flex-direction: row;
  margin: 18.2px 28px 0px 288px;
  padding: 0px;
  display: flex;
  justify-content: flex-end;
  border: 1px solid #ebe9f1;
  border-radius: 0.428rem;
  z-index: 11;
}
.nav-content {
  box-sizing: border-box;
  border-radius: 0.428rem;
  display: flex;
  width: 1201.2px;
  height: 62.4px;
  font-size: 14px;
  font-weight: 400;
  line-height: 20.3px;
  padding: 11.2px 14px;
  letter-spacing: 0.14px;
  text-align: left;
  align-items: center;
  background-color: white;
  box-shadow: 0 2px 8px 0 rgb(34 41 47 / 14%);
}
.navbar-left {
  box-sizing: border-box;
  width: 761.862px;
  font-size: 14px;
}
.navbar-right {
  margin-left: 80px;
  margin-top: 0px;
  padding-right: 12.5px;
  width: 439.338px;
  display: flex;
  justify-content: flex-end;
}
/* .navbar-right ul li {
    padding: 0px 3.5px;
} */
.icons-left,
.icons-right {
  display: flex;
  align-items: center;
  height: 40px;
  padding: 0px;
  font-size: 13px;
  list-style: none;
}
.imggg {
  padding: 0px 7px;
  margin-top: 4px;
}

.icon {
  box-sizing: border-box;
  width: 21px;
  height: 22.1px;
  font-size: 14px;
  padding: 0px 7px;
}
.star {
  color: #ff9f43;
}
.span {
  display: block;
  padding: 0px 7px;
  letter-spacing: 1px;
}
.account {
  width: 40px;
}
.notification {
  position: relative;
}
.star-menu {
  padding: 7px 0px;
  width: 300px;
  /* height:228.79px ; */
  list-style: none;
  background-color: white;
  border: 1px solid #ebe9f1;
  position: absolute;
  left: 0px;
  top: 50px;
  border-radius: 0.357rem;
  color: #6e6b7b;
}
.display {
  display: none;
}
ul li {
  cursor: pointer;
}
.notification::before {
  content: "";
  position: absolute;
  bottom: 17px;
  left: 17px;
  border: 9.5px solid transparent;
  border-radius: 50%;
  /* transform: translateY(-90%); */
  /* transform: translateX(-70%); */
  border-color: #ea5455;
}
.notification::after {
  content: "6";
  position: absolute;
  bottom: 16px;
  left: 23px;
  font-size: 12px;
  font-weight: 600;
  color: white;
}

.cart {
  position: relative;
}
.cart::before {
  content: "";
  position: absolute;
  bottom: 17px;
  left: 17px;
  border: 9.5px solid transparent;
  border-radius: 50%;
  border-color: #7367f0;
}
.cart::after {
  content: "5";
  position: absolute;
  bottom: 16px;
  left: 23px;
  font-size: 12px;
  font-weight: 600;
  color: white;
}
.star {
  position: relative;
}
.john {
  line-height: 14px;
  padding-left: 2px;
  display: flex;
  flex-direction: column;
}
.star-menu li {
  padding: 9.1px 11px;
  height: 23.5px;
}
.hov {
  height: 23.5px;
}
.hov:hover {
  background-color: #7267f044;
}
.star-menu .star-search {
  padding: 14px;
  padding-bottom: 20px;
}
.star-menu .star-search input {
  padding: 0.438rem 1rem;
  height: 37.99px;
  background-color: #fff;
  border: 1px solid #d8d6de;
  border-radius: 0.357rem;
  width: 100%;
  font-size: 14px;
}
::-webkit-input-placeholder {
  color: #bebec8;
}
.star-icon {
  width: 18px;
  height: 18px;
}
.list-icon {
  float: right;
  width: 16px;
}
.admin {
  font-size: 12px;
  font-weight: 400;
  letter-spacing: 0px;
  margin-left: 60%;
  transform: translateX(-60%);
}
.imgg img {
  width: 40px;
  height: 40px;
  border-radius: 50%;
}
.imgg {
  position: relative;
}
.imgg::after {
  content: "";
  position: absolute;
  top: 2.5px;
  left: 35.5px;
  border: 5px solid transparent;
  border-radius: 50%;
  border-color: #28c76f;
}
.doe {
  font-weight: bold;
}
.eng {
  letter-spacing: 0px;
  font-size: 14px;
  font-weight: 420;
}
.shop-container {
  position: absolute;
  display: flex;
  width: 895.4px;
  height: 33.4px;
  margin: 107.5px 309px 0px 288px;
}
.shop h2 {
  margin-top: 0;
  width: 63.4px;
  height: 28.8px;
  border-right: 1px solid #d6dce1;
  padding-right: 14px;
  color: rgb(99, 99, 99);
  font-size: 23.996px;
  font-weight: 500;
}
.shop-icons {
  display: flex;
  list-style: none;
  margin-top: 4.5px;
  padding-left: 14.5px;
}
.shop-icons li {
  width: 0;
  padding-right: 25.5px;
  font-size: 12px;
  padding-top: 3px;
}
.house {
  font-size: 14px;
  color: #7367f0;
}
.shop {
  display: flex;
}
.shop-icons .ec {
  width: 75px;
  margin-left: -10px;
  font-size: 14px;
  color: #7367f0;
}
.shop-icons .sh {
  font-size: 14px;
  color: #6e6b7b;
}
.shop-container .arr2 {
  padding-right: 15px;
}
</style>
