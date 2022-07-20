<template>
  <div class="filters-container">
    <div class="fil">
      <div class="filters-text">
        <h6>Filters</h6>
      </div>
    </div>
    <div class="filters-body">
      <div class="multi-range-price">
        <h6>Multi Range</h6>
        <div class="price-group">
          <div class="price">
            <input type="radio" name="num" class="radio-price" id="p1" value="all" />
            <label for="p1"><span class="price-text">All</span></label>
          </div>
          <div class="price">
            <input type="radio" name="num" class="radio-price" id="p1" value="all" />
            <label for="p1"><span class="price-text"> &lt;=$10 </span></label>
          </div>
          <div class="price">
            <input type="radio" name="num" class="radio-price" id="p1" value="all" />
            <label for="p1"><span class="price-text">$10 - $100</span></label>
          </div>
          <div class="price">
            <input type="radio" name="num" class="radio-price" id="p1" value="all" />
            <label for="p1"><span class="price-text">$100 - $500</span></label>
          </div>
          <div class="price">
            <input type="radio" name="num" class="radio-price" id="p1" value="all" />
            <label for="p1"><span class="price-text">&gt;=$500</span></label>
          </div>
        </div>
      </div>
      <div class="multi-range-price">
        <h6>Price Range</h6>
        <div slider id="slider-distance">
          <div>
            <div inverse-left style="width: 70%"></div>
            <div inverse-right style="width: 70%"></div>
            <div range style="left: 0%; right: 0%"></div>
            <span thumb style="left: 0%"></span>
            <span thumb style="left: 100%"></span>
            <div sign style="left: 0%">
              <span id="value">0</span>
            </div>
            <div sign style="left: 100%">
              <span id="value">100</span>
            </div>
          </div>
          <input
            type="range"
            value="0"
            max="100"
            min="0"
            step="1"
            @input="
              this.value = Math.min(
                this.value,
                this.parentNode.childNodes[5].value - 1
              );
              let value = (this.value / parseInt(this.max)) * 100;
              var children = this.parentNode.childNodes[1].childNodes;
              children[1].style.width = value + '%';
              children[5].style.left = value + '%';
              children[7].style.left = value + '%';
              children[11].style.left = value + '%';
              children[11].childNodes[1].innerHTML = this.value;
            "
          />

          <input
            type="range"
            value="100"
            max="100"
            min="0"
            step="1"
            @input="
              this.value = Math.max(
                this.value,
                this.parentNode.childNodes[3].value - -1
              );
              let value = (this.value / parseInt(this.max)) * 100;
              var children = this.parentNode.childNodes[1].childNodes;
              children[3].style.width = 100 - value + '%';
              children[5].style.right = 100 - value + '%';
              children[9].style.left = value + '%';
              children[13].style.left = value + '%';
              children[13].childNodes[1].innerHTML = this.value;
            "
          />
        </div>
      </div>
      <div class="multi-range-price">
        <h6>Categories</h6>
        <div class="price-group">
          <div class="price">
            <input type="radio" name="categ" class="radio-price" id="p1" value="all" />
            <label for="p1"><span class="price-text">Appliances</span></label>
          </div>
          <div class="price">
            <input type="radio" name="categ" class="radio-price" id="p1" value="all" />
            <label for="p1"><span class="price-text"> Appliances </span></label>
          </div>
          <div class="price">
            <input type="radio" name="categ" class="radio-price" id="p1" value="all" />
            <label for="p1"
              ><span class="price-text">Cameras &amp; Camcorders</span></label
            >
          </div>
          <div class="price">
            <input type="radio" name="categ" class="radio-price" id="p1" value="all" />
            <label for="p1"
              ><span class="price-text">Cameras &amp; Camcorders</span></label
            >
          </div>
          <div class="price">
            <input type="radio" name="categ" class="radio-price" id="p1" value="all" />
            <label for="p1"><span class="price-text">Cell Phones</span></label>
          </div>
          <div class="price">
            <input type="radio" name="categ" class="radio-price" id="p1" value="all" />
            <label for="p1"
              ><span class="price-text">Computers &amp; Tablets</span></label
            >
          </div>
          <div class="price">
            <input type="radio" name="categ" class="radio-price" id="p1" value="all" />
            <label for="p1"
              ><span class="price-text">
                Health, Fitness &amp; Beauty
              </span></label
            >
          </div>
          <div class="price">
            <input type="radio" name="categ" class="radio-price" id="p1" value="all" />
            <label for="p1"
              ><span class="price-text"
                >Office &amp; School Supplies</span
              ></label
            >
          </div>
          <div class="price">
            <input type="radio" name="categ" class="radio-price" id="p1" value="all" />
            <label for="p1"
              ><span class="price-text">TV &amp; Home Theater</span></label
            >
          </div>
          <div class="price">
            <input type="radio" name="categ" class="radio-price" id="p1" value="all" />
            <label for="p1"><span class="price-text">Video Games</span></label>
          </div>
        </div>
      </div>
      <div class="multi-range-price">
        <h6>Brands</h6>
        <div class="price-group">
            <div class="price">
            <input type="radio" name="bullets" checked  v-model="brandinp" @change="brandFilter" class="radio-price" id="0" value="" />
            <label for="0"><span class="price-text">All</span></label>
          </div>
          <div class="price">
            <input type="radio" name="bullets"  v-model="brandinp" @change="brandFilter" class="radio-price" id="1" value="Insignia™" />
            <label for="1"><span class="price-text">Insignia™</span></label>
          </div>
          <div class="price">
            <input type="radio" name="bullets" v-model="brandinp" @change="brandFilter" class="radio-price" id="2" value="Samsung" />
            <label for="2"><span class="price-text"> Samsung </span></label>
          </div>
          <div class="price">
            <input type="radio" name="bullets" v-model="brandinp" @change="brandFilter" class="radio-price" id="3" value="Matra" />
            <label for="3"><span class="price-text">Matra</span></label>
          </div>
          <div class="price">
            <input type="radio" name="bullets" v-model="brandinp" @change="brandFilter" class="radio-price" id="4" value="HP" />
            <label for="4"><span class="price-text">HP</span></label>
          </div>
          <div class="price">
            <input type="radio" name="bullets" v-model="brandinp" @change="brandFilter" class="radio-price" id="5" value="Apple" />
            <label for="5"><span class="price-text">Apple</span></label>
          </div>
          <div class="price">
            <input type="radio" name="bullets" v-model="brandinp" @change="brandFilter" class="radio-price" id="6" value="GE" />
            <label for="6"><span class="price-text">GE</span></label>
          </div>
          <div class="price">
            <input type="radio" name="bullets" v-model="brandinp" @change="brandFilter" class="radio-price" id="7" value="Sony" />
            <label for="7"><span class="price-text"> Sony </span></label>
          </div>
          <div class="price">
            <input type="radio" name="bullets" v-model="brandinp" @change="brandFilter" class="radio-price" id="8" value="Incipio" />
            <label for="8"><span class="price-text">Incipio</span></label>
          </div>
          <div class="price">
            <input type="radio" name="bullets" v-model="brandinp" @change="brandFilter" class="radio-price" id="9" value="KitchenAid" />
            <label for="9"><span class="price-text">KitchenAid</span></label>
          </div>
          <div class="price">
            <input type="radio" name="bullets" v-model="brandinp" @change="brandFilter" class="radio-price" id="10" value="Whirlpool" />
            <label for="10"><span class="price-text">Whirlpool</span></label>
          </div>
        </div>
      </div>
      <div class="multi-range-price">
        <h6>Rating</h6>
        <div class="price-group">
          <div class="price">
            <i class="star-icn fa-solid colored fa-star light light"></i>
            <i class="star-icn fa-solid colored fa-star light light"></i>
            <i class="star-icn fa-solid colored fa-star light light"></i>
            <i class="star-icn fa-solid colored fa-star light light"></i>
            <i class="star-icn fa-regular fa-star light light"></i>
            <span class="txt1">& up</span>
            <span class="txt2">160</span>
          </div>
          <div class="price">
            <i class="star-icn fa-solid colored fa-star light light"></i>
            <i class="star-icn fa-solid colored fa-star light light"></i>
            <i class="star-icn fa-solid colored fa-star light light"></i>
            <i class="star-icn fa-regular fa-star light light"></i>
            <i class="star-icn fa-regular fa-star light light"></i>
            <span class="txt1">& up</span>
            <span class="txt2">176</span>
          </div>
          <div class="price">
            <i class="star-icn fa-solid colored fa-star light light"></i>
            <i class="star-icn fa-solid colored fa-star light light"></i>
            <i class="star-icn fa-regular fa-star light light"></i>
            <i class="star-icn fa-regular fa-star light light"></i>
            <i class="star-icn fa-regular fa-star light light"></i>
            <span class="txt1">& up</span>
            <span class="txt2">291</span>
          </div>
          <div class="price">
            <i class="star-icn fa-solid colored fa-star light light"></i>
            <i class="star-icn fa-regular fa-star light light"></i>
            <i class="star-icn fa-regular fa-star light light"></i>
            <i class="star-icn fa-regular fa-star light light"></i>
            <i class="star-icn fa-regular fa-star light light"></i>
            <span class="txt1">& up</span>
            <span class="txt2">190</span>
          </div>

        </div>
      </div>
    </div>
  </div>
</template>

<script>
 export default {
  data(){
    return{
    brandinp:"",
  }
  },
methods :{

  brandFilter(){
    this.$emit("brandinp",this.brandinp)
  },

}
};

</script>

<style>
.star-icn{
    padding: 0;
}
.txt1{
    margin-left: 4px;
    font-size: 14px;
    color: #7367f0;
    cursor: pointer;
}
.txt2{
    margin-left: 62px;
    font-size: 14px;
    font-weight: 400;
    color: #6e6b7b;
}
.colored{
    color: orange;
}
[slider] {
  width: 220px;
  position: relative;
  height: 5px;
  margin: 45px 0 10px 0;
}

[slider] > div {
  position: absolute;
  left: 13px;
  right: 15px;
  height: 5px;
}
[slider] > div > [inverse-left] {
  position: absolute;
  left: 0;
  height: 5px;
  border-radius: 10px;
  background-color: #ccc;
  margin: 0 7px;
}

[slider] > div > [inverse-right] {
  position: absolute;
  right: 0;
  height: 5px;
  border-radius: 10px;
  background-color: #ccc;
  margin: 0 7px;
}

[slider] > div > [range] {
  position: absolute;
  left: 0;
  height: 5px;
  border-radius: 14px;
  background-color: #7367f0;
}

[slider] > div > [thumb] {
  position: absolute;
  top: -7px;
  z-index: 2;
  height: 20px;
  width: 20px;
  text-align: left;
  margin-left: -11px;
  cursor: pointer;
  box-shadow: 0 3px 8px rgba(0, 0, 0, 0.4);
  background-color: #fff;
  border-radius: 50%;
  outline: none;
}

[slider] > input[type="range"] {
  position: absolute;
  pointer-events: none;
  -webkit-appearance: none;
  z-index: 3;
  height: 14px;
  top: -2px;
  width: 100%;
  opacity: 0;
}

div[slider] > input[type="range"]:focus::-webkit-slider-runnable-track {
  background: transparent;
  border: transparent;
}

div[slider] > input[type="range"]:focus {
  outline: none;
}

div[slider] > input[type="range"]::-webkit-slider-thumb {
  pointer-events: all;
  width: 28px;
  height: 28px;
  border-radius: 0px;
  border: 0 none;
  background: #7367f0;
  -webkit-appearance: none;
}

div[slider] > input[type="range"]::-ms-fill-lower {
  background: transparent;
  border: 0 none;
}

div[slider] > input[type="range"]::-ms-fill-upper {
  background: transparent;
  border: 0 none;
}

div[slider] > input[type="range"]::-ms-tooltip {
  display: none;
}

[slider] > div > [sign] {
  opacity: 0;
  position: absolute;
  margin-left: -11px;
  top: -39px;
  z-index: 3;
  background-color: #7367f0;
  color: #fff;
  width: 28px;
  height: 28px;
  border-radius: 28px;
  -webkit-border-radius: 28px;
  align-items: center;
  -webkit-justify-content: center;
  justify-content: center;
  text-align: center;
}

[slider] > div > [sign]:after {
  position: absolute;
  content: "";
  left: 0;
  border-radius: 16px;
  top: 19px;
  border-left: 14px solid transparent;
  border-right: 14px solid transparent;
  border-top-width: 16px;
  border-top-style: solid;
  border-top-color: #7367f0;
}

[slider] > div > [sign] > span {
  font-size: 12px;
  font-weight: 700;
  line-height: 28px;
}

[slider]:hover > div > [sign] {
  opacity: 1;
}
.filters-container {
  position: absolute;
  width: 260px;
  margin-left: 288px;
  margin-top: 172.9px;
}
.fil {
  display: flex;
  justify-content: left;
  height: 41.3px;
}
.filters-text h6 {
  margin-top: 3px;
  color: #5e5873;
  font-size: 14px;
  font-weight: 500;
}
.filters-body {
  box-sizing: border-box;
  width: 100%;
  background-color: #ffffff;
  border: 1px solid #ebe9f1;
  border-radius: 5px;
  padding: 21px;
}
.multi-range-price {
  margin-bottom: 35px;
}
.multi-range-price h6 {
  color: #5e5873;
  font-size: 14px;
  font-weight: 500;
  margin: 0 0 14px;
}
.price {
  display: flex;
  align-items: center;
  margin-bottom: 10px;
}
.price-text {
  font-size: 14px;
  color: #5e5873;
  padding-left: 5px;
}
.radio-price {
  width: 18px;
  height: 18px;
  margin: 0;
}
</style>
