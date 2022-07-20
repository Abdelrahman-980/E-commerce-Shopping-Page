<template>
    <div class="drawer-container">
        <div class="logo-container">
            <ul class="logo-list">
                <li class="logo">
                <img
                    class="logo-img"
                    src="https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/logo.36f34a9f.svg"
                    alt="logo"
                />
                <h2 class="logo-text">Vuexy</h2>
                </li>
                <li>
                <div class="drawer-icon"></div>
                </li>
            </ul>
            </div>
            <ul class="dash-icon">
            <li class="logo">
                <i class="fa-solid fa-house"></i>
                <p class="dash-text">Dashboards</p>
                <i class="fa-solid arrow-icon fa-angle-right"></i>
            </li>
            <li>
                <p class="apps">APPS &amp; PAGES</p>
            </li>

            <li class="dash-item">
                <a href="#">
                <i class="itm-icn fa-regular fa-envelope"></i>
                <span>Email</span>
                </a>
            </li>
            <li class="dash-item">
                <a href="#">
                <i class="itm-icn fa-regular fa-message"></i>
                <span>Chat</span>
                </a>
            </li>
            <li class="dash-item">
                <a href="#">
                <i class="itm-icn fa-regular fa-calendar-check"></i>
                <span>Todo</span>
                </a>
            </li>
            <li class="dash-item">
                <a href="#">
                <i class="itm-icn fa-regular fa-calendar"></i>
                <span>Calender</span>
                </a>
            </li>
            <li class="dash-item">
                <a href="#">
                <i class="itm-icn fa-regular fa-file-lines"></i>
                <span>Invoice</span>
                </a>
            </li>
            <li class="dash-item">
                <a href="#">
                <i class="itm-icn fa-solid fa-cart-shopping"></i>
                <span>eCommerce</span>
                </a>
            </li>
            <li class="dash-item">
                <a href="#">
                <i class="itm-icn fa-regular fa-user"></i>
                <span>User</span>
                </a>
            </li>
            <li class="dash-item">
                <a href="#">
                <i class="itm-icn fa-regular fa-file"></i>
                <span>Pages</span>
                </a>
            </li>

            <li>
                <p class="apps">USER INTERFACE</p>
            </li>

            <li class="dash-item">
                <a href="#">
                <i class="itm-icn fa-solid fa-t"></i>
                <span>Typography</span>
                </a>
            </li>
            <li class="dash-item">
                <a href="#">
                <i class="itm-icn fa-solid fa-droplet"></i>
                <span>Colors</span>
                </a>
            </li>
            <li class="dash-item">
                <a href="#">
                <i class="itm-icn fa-solid fa-eye"></i>
                <span>Feather</span>
                </a>
            </li>
            <li class="dash-item">
                <a href="#">
                <i class="itm-icn fa-solid fa-credit-card"></i>
                <span>Cards</span>
                </a>
            </li>
            <li class="dash-item">
                <a href="#">
                <i class="itm-icn fa-solid fa-box-archive"></i>
                <span>Components</span>
                </a>
            </li>
            <li class="dash-item">
                <a href="#">
                <i class="itm-icn fa-solid fa-circle-plus"></i>
                <span>Extensions</span>
                </a>
            </li>
            <li class="dash-item">
                <a href="#">
                <i class="itm-icn fa-solid fa-table-columns"></i>
                <span>Page layouts</span>
                </a>
            </li>
        </ul>
    </div>
</template>

<script>
export default {};
</script>

<style>
.drawer-container {
  position: fixed;
  margin: 0px;
  padding: 0;
  box-sizing: border-box;
  width: 260px;
  background-color: rgb(255, 255, 255);
  box-shadow: 0 0 15px 0 rgb(34 41 47 / 5%);
}
.logo-container {
  width: 223.04px;
  height: 53.2px;
  padding: 4.9px 14px 4.2px 22.96px;
}
.logo-list {
  height: 62.3px;
  padding: 0;
  margin: 0;
  list-style: none;
}
.logo {
  width: 127.738px;
  height: 63.975px;
  display: flex;
  justify-content: flex-start;
  align-items: center;
}
.logo-img {
  width: 36px;
  height: 24.48px;
  margin-top: 2px;
}
.logo-text {
  margin: 0;
  font-size: 20.3px;
  font-weight: 600;
  padding-left: 14px;
  color: rgb(115, 103, 240);
}
.logo-text::before {
  content: "";
  position: absolute;
  top: 30px;
  left: 220px;
  border: 9.8px solid transparent;
  border-radius: 50%;
  border-color: #7367f0;
}
.logo-text::after {
  content: "O";
  position: absolute;
  top: 24.5px;
  left: 221.4px;
  font-size: 20px;
  font-weight: bolder;
  color: white;
}
.dash-icon {
  margin: 0;
  padding-left: 30px;
  margin-bottom: 30px;
}
.dash-icon li {
  list-style: none;
}
.dash-text {
  position: relative;
  padding-left: 15.4px;
  padding-top: 3px;
}
.dash-text::before {
  content: "";
  position: absolute;
  top: 6px;
  left: 145px;
  border: 10px solid transparent;
  border-radius: 50%;
  border-color: #f9ede2;
}
.dash-text::after {
  content: "2";
  position: absolute;
  top: 6.8px;
  left: 151.5px;
  font-size: 13px;
  font-weight: 600;
  color: #ff9f43;
}
.arrow-icon {
  font-size: 12px;
  margin-top: 4px;
  margin-left: 70px;
}
.apps {
  font-size: 12.5px;
  font-weight: 500;
  color: #a6a4b0;
}
.dash-item {
  box-sizing: border-box;
  height: 42.33px;
  transition: 0.2s ease-in-out;
}
.dash-item:hover {
  margin-left: 6px;
}
.dash-item a {
  cursor: pointer;
  display: flex;
  font-weight: 400;
  text-decoration: none;
  align-items: center;
}
.dash-item .itm-icn {
  width: 18px;
  height: 18px;
  padding-right: 15px;
  color: #6e6b7b;
}
.dash-item span {
  cursor: pointer;
  color: #6e6b7b;
  font-size: 15.4px;
  letter-spacing: 1.14px;
  line-height: 22.3px;
}
</style>