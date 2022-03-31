<template>
  <div class="content-container">
    <header>
      <div class="header-left">
        <h2>Shop</h2>
        <div>
          <span class="material-icons-outlined">home</span>
          <span class="material-icons-outlined">chevron_right</span>
          <span>ECommerce</span>
          <span class="material-icons-outlined">chevron_right</span>
          <span>Shop</span>
        </div>      
      </div>
      <div class="header-right">
        <a href=""><span class="material-icons-outlined">settings</span></a>   
      </div>
    </header>
    <main>
      <div class="contain">
        <div class="filter">
          <!--Multi range -->
          <div class="filter-title">
            <h6>Filters</h6>
          </div>
          <div class="filter-body">
            <div class="multi-range">
              <div><h6>Multi Range</h6></div>
              <div>
                <input type="radio" name="mrange" id="all">
                <label for="all">All</label>
              </div>
              <div>
                <input type="radio" name="mrange" id="lt10">
                <label for="lt10">&lt;&#61; &#36;10</label>
              </div>
              <div>
                <input type="radio" name="mrange" id="to100">
                <label for="to100">&#36;10 - &#36;100</label>
              </div>
              <div>
                <input type="radio" name="mrange" id="to500">
                <label for="to100">&#36;100 - &#36;500</label>
              </div>
              <div>
                <input type="radio" name="mrange" id="lt10">
                <label for="lt10">&gt;&#61; &#36;590</label>
              </div>
          </div>
          <!--price range -->
          <div class="price-range">
            <div><h6>Price Range</h6></div>
            <div class="range-input">
              <input type="range" name="" id="">
            </div>          
          </div>
          <!--categories -->
          <div class="categories">
            <div><h6>Categories</h6></div>
            <div>
              <input type="radio" name="catg" id="">
              <label for="">Appliances</label>
            </div>
            <div>
              <input type="radio" name="catg" id="">
              <label for="">Aduio</label>
            </div>
            <div>
              <input type="radio" name="catg" id="">
              <label for="">Cameras &amp; Camcorders</label>
            </div>
            <div>
              <input type="radio" name="catg" id="">
              <label for="">Cars Electronics &amp; GPA</label>
            </div>
            <div>
              <input type="radio" name="catg" id="">
              <label for="">Cell Phones</label>
            </div>
          </div>
          <!--brands -->
          <div class="brands">
            <div><h6>Brands</h6></div>
            <div>
              <input type="radio" name="brand" id="">
              <label for="">Insignia<sup>TM</sup></label>
            </div>
            <div>
              <input type="radio" name="brand" id="">
              <label for="">Samsung</label>
            </div>
            <div>
              <input type="radio" name="brand" id="">
              <label for="">Metra</label>
            </div>
            <div>
              <input type="radio" name="brand" id="">
              <label for="">HP</label>
            </div>
            <div>
              <input type="radio" name="brand" id="">
              <label for="">Apple</label>
            </div>
          </div>
          <!--ratings -->
          <div class="ratings">
            <div><h6>Ratings</h6></div>
            <div>
              <div>
                <i class="fa-duotone fa-star"></i>
                <i class="fa-duotone fa-star"></i>
                <i class="fa-duotone fa-star"></i>
                <i class="fa-duotone fa-star"></i>
                <i class="fa-light fa-star"></i>
                &amp; up</div>
              <span>160</span>
            </div>
            <div>
              <div>
                <i class="fa-solid fa-star-sharp"></i>
                <i class="fa-solid fa-star-sharp"></i>
                <i class="fa-duotone fa-star"></i>
                <i class="fa-light fa-star"></i>
                <i class="fa-light fa-star-sharp"></i>
                &amp; up
              </div>
              <span>176</span>
            </div>
            <div>
              <div>&amp; up</div>
              <span>291</span>
            </div>
            <div>
              <div>&amp; up</div>
              <span>190</span>
            </div>
          </div>
          </div>

        </div>
        <div class="results">
          <div class="sort">
            <div class="sort-title">
              <h6>27 Results Found</h6>
              <button @click="openMenu"><span class="material-icons-outlined">reorder</span></button>
            </div>
            <div class="sort-body">
              <select name="" id="">
                <option value="">Featured</option>
                <option value="">Highest</option>
                <option value="">Lowest</option>
              </select>
              <div class="sort-buttons">
                <button><span class="material-icons-outlined">grid_view</span></button>
                <button><span class="material-icons-outlined">format_list_bulleted</span></button>           
              </div>
            </div>
          </div>
          <div class="search">
            <input type="search" name="" id="" placeholder="Search Product" v-model="searchValue" @keyup="addProduct">
          </div>
          <div class="products">
            <!--search result-->
            <div class="product-item" v-if="searchProducts.length>0" v-for="product in searchProducts" :key="product.id">
              <div class="img">
                <img :src="product.img" alt="">
              </div>
              <div class="product-body">
                <div class="top-body">
                  <div class="rating">
                    <div class="stars">
                      <span class="material-icons-outlined">star_border_purple500</span>
                      <span class="material-icons-outlined">star_border_purple500</span>
                      <span class="material-icons-outlined">star_border_purple500</span>
                      <span class="material-icons-outlined">star_border_purple500</span>
                      <span class="material-icons-outlined">star_border_purple500</span> 
                    </div>
                    <div class="price"><span>&#36;{{product.price}}</span></div>
                  </div>
                  <div class="title">
                    <h4>{{product.name}}</h4>
                    <p>{{product.discription}}</p>
                  </div>
                </div>              
                <div class="shop">
                  <div class="fav"><span class="material-icons-outlined">favorite_border</span><span>Wishlist</span></div>
                  <div class="cart"><span class="material-icons-outlined">shopping_cart</span><span>View In Cart</span></div>
                </div>
              </div>           
            </div>
            <div class="product-item" v-else v-for="product in products" :key="product.id">
              <div class="img">
                <img :src="product.img" alt="">
              </div>
              <div class="product-body">
                <div class="top-body">
                  <div class="rating">
                    <div class="stars">
                      <span class="material-icons-outlined">star_border_purple500</span>
                      <span class="material-icons-outlined">star_border_purple500</span>
                      <span class="material-icons-outlined">star_border_purple500</span>
                      <span class="material-icons-outlined">star_border_purple500</span>
                      <span class="material-icons-outlined">star_border_purple500</span> 
                    </div>
                    <div class="price"><span>&#36;{{product.price}}</span></div>
                  </div>
                  <div class="title">
                    <h4>{{product.name}}</h4>
                    <p>{{product.discription}}</p>
                  </div>
                </div>              
                <div class="shop">
                  <div class="fav"><span class="material-icons-outlined">favorite_border</span><span>Wishlist</span></div>
                  <div class="cart"><span class="material-icons-outlined">shopping_cart</span><span>View In Cart</span></div>
                </div>
              </div>           
            </div>        
          </div>
        </div>
      </div>
    </main>
  </div>
</template>

<script>
import {computed, ref} from 'vue'
export default {
  //showFilter:false,
  data(){
    return {
      searchValue:'',
      searchProducts:[],
      products:[]
      }
  },
  mounted(){
    fetch('http://localhost:3000/products')
      .then(res=>res.json())
      .then(data=>this.products=data)
      .catch(err=>console.log(err.message))
  },
  computed:{
    addProduct(){
      if(this.searchValue!=''){
        const resultProduct=this.products.filter(product=>{
          if(product.name.toLowerCase().includes(this.searchValue)){
            return product  
          }  
        })
        this.searchProducts=resultProduct
        
      }
    }
    
  },
  methods:{
    openMenu(){
      this.showFilter=true
    } 
  }
}
</script>

<style scoped>
*{
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
header{
  line-height: 1.45;
  margin-bottom: 1.5rem!important;
}
header,header .header-left,header .header-right{
  display: flex;
  flex-direction: row;
  align-content: center;
  justify-content: space-between;
}
header .header-left{
  padding-right: 1rem;
}
header .header-left h2{
  border-right: 1px solid #d6dce1;
  font-weight: 500;
  color: #636363;
  padding-right: 1rem!important;
  font-size: 1.714rem;
}
header .header-left div{
  padding: 0.3rem 1rem;
  font-size: 1rem;
  display: flex;
  align-items: center;
}
header .header-left div i,header .header-left div span{
  padding-left: .6rem;
  color: #6e6b7b;
}
header .header-right{
  background-color: #7367f0!important;
  width: 38.5px;
  height: 38.5px;
  text-align: center;
  display: flex;
  justify-content: center;
  align-items: center;
  border: 1px solid #7367f0;
  border-radius: 4px;
}
header .header-right a{
  display: flex;
  align-items: center;
}
header .header-right a span{
  color: #fff;
  font-weight: smaller;
  font-size: 1rem;
}

main .contain{
  display: flex;
  justify-content: space-between;
}
main .contain .filter{
  width: 20%;
  margin-top: 1rem;
}
main .contain .filter .filter-title{
  text-align: left;
  padding-right:1rem;
}
main .contain .filter h6,.results .sort h6{
  margin-bottom: 1.75rem;
  margin-top: 0;
  font-size: 1rem;
  font-family: inherit;
  font-weight: 500;
  line-height: 1.2;
  color: #5e5873;
}
main .contain .filter .filter-body{
  background-color: #fff;
  padding: 1.5rem;
  border-radius: 5px;
  box-shadow:0 4px 24px 0 rgb(34 41 47 / 10%)
}
main .contain .filter .filter-body h6{
  margin: 0;
}
:is(.multi-range,.price-range,.categories,.brands,.ratings) div{
  display: flex;
  justify-content:flex-start;
  align-items: center;
  color:#5e5873;
  margin-bottom: 0.75rem;
}
input[type='radio']{
   margin-right: .6rem;
}
 input[type='radio']:after {
  width: 15px;
  height: 15px;
  border-radius: 15px;
  top: -2px;
  left: -1px;
  position: relative;
  background-color: #fff;
  content: '';
  display: inline-block;
  visibility: visible;
  border: 1px solid rgb(206, 206, 206);
       
}

input[type='radio']:checked:after {
  width: 15px;
  height: 15px;
  border-radius: 15px;
  top: -2px;
  left: -1px;
  position: relative;
  background-color :#7367f0;
  content: '';
  display: inline-block;
  visibility: visible;
  border: 2px solid white;
}
main .contain .filter .price-range .range-input{
  padding: 7px 0px; 
  width: auto;
  height: 4px;
  position: relative;
  user-select: none;
  
}
 

.results{
  display:flex;
  flex-direction: column;
  width: 77%;
  border-radius: 2px;
}
.results .sort{
  display: flex;
  justify-content: space-between;
  align-content: center;
  width: 100%;  
}
.results .sort .sort-body{
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.results .search{
  margin-top: 1rem;
}
.results .search input{
  width: 100%;
  box-shadow: 0 4px 24px 0 rgb(34 41 47 / 10%);
  outline: none;
  border: none;
  border-radius: 4px;
  height: 3rem;
  padding-left: 1.25rem;
}
.results .products{
  display:grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(3, 1fr);
  column-gap:1rem;
  margin-top: 2rem;
}
.results .products .product-item{
  background-color: #fff;
  box-shadow: 0 4px 24px 0 rgb(34 41 47 / 10%);
  border: none;
  margin-bottom: 2rem;
  border-radius: 0.428rem;
  position: relative;
  display: flex;
  -webkit-box-orient: vertical;
  -webkit-box-direction: normal;
  -ms-flex-direction: column;
  flex-direction: column;
  min-width: 0;
  word-wrap: break-word;
 
}
.results .products .product-item img{
  width: 100%;
  height: auto;
}
.results .products .product-item .product-body .top-body{
  padding: 1rem;
}
.results .products .product-item .rating{
  display: flex;
  justify-content: space-between;
  align-content: center;
  align-items: center;
}
.results .products .product-item .rating .stars{
  display: flex;
}
.results .products .product-item .rating .stars .material-icons-outlined{
  color:#ff9f4f;
  font-weight: 100;
  padding-right: .2rem;
}
.results .products .product-item .rating .price{
  font-weight: 600 !important;
  font-size: .9rem !important;
  color: #636363;
}
.results .products .product-item p,.results .products .product-item h4{
  margin: 0;
  padding: 0;
  font-weight: 400;
  text-align: left;
  color: #6e6b7b;
  margin-top: .5rem;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
  font-size: .9rem;
}
.results .products .product-item h4{
  font-weight: 600;
  font-size: .9rem;
}
.results .products .product-item .product-body .shop,.results .products .product-item .product-body .fav,.results .products .product-item .product-body .cart{
  width: 100%;
  display: flex;
  align-items: center;
  color: #2a2e30;
  flex-direction: column;
}
.results .products .product-item .product-body .shop div{
  flex-direction: row;
  justify-content: center;
}
.results .products .shop div{
  border: 1px solid transparent;
  padding: 0.786rem 1.5rem; 
  font-size: .8rem;
}
.results .products .shop .cart{
  background-color:#7367f0;   
}
.results .products .shop .fav{
  background-color: #f6f6f6;
}
 .results .products .shop .cart span{
   color: white;
 }
 .results .products .shop .cart span:nth-child(1),.results .products .shop .fav span:nth-child(1){
   font-size: 1.4rem;
   font-weight: smaller;
   margin-right: .5rem;
 }
.results select{
  color: #7367f0;
  border: 1px solid #7367f0!important;
  background-color: transparent;
  padding: 0.786rem 1.5rem !important;
  border-radius: .358rem;
  outline: none;
  text-align: center;
  font-weight: 500 !important;
   background-color: rgba(115,103,240,.2);
}
.results .sort-buttons{
  margin-left: 1rem;
  display: inline-flex;
  vertical-align: middle;
}
.results .sort-buttons button{
  outline: none;
  border: 1px solid #7367f0;
  padding: 0.486rem 1rem;
  border-radius: 0.358rem;
}
.results .sort-buttons button:active{
  background-color: rgba(115,103,240,.2);
}
.results .sort-buttons button span{
  color: #6934E3;
}
.results .sort-buttons button:nth-child(1){
  border-top-right-radius: 0;
  border-bottom-right-radius: 0;
}
.results .sort-buttons button:nth-child(2){
  border-top-left-radius: 0;
  border-bottom-left-radius: 0;
}
/*====================================responsive filter bar=========================== */
.results .sort-title button{
  background-color: transparent;
  border: none;
  outline: none;
}
@media only screen and (max-width: 992px){
  .contain .filter{
    display: none;
  }
  .results h6{
    display: none;
  }
  .results .sort-title button{
    display: block;
  }
  .results .products{
  grid-template-columns: repeat(2, 1fr);
  grid-template-rows: repeat(2, 1fr);
  }
}
@media only screen and (min-width: 992px){
.results .sort-title button{
    display: none;
  }

}
@media only screen and (max-width: 567px){
  .results .products{
  grid-template-columns: repeat(1, 1fr);
  grid-template-rows: repeat(1, 1fr);
  }
}
</style>

 