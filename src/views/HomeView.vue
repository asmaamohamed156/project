<template>
  <div class="home">  
     <aside  v-if="!showMenu">
       <div class="navbar-header">
         <ul>
           <li>
             <router-link :to="{name:'home'}" class="nav-brand">
               <img src="../assets/images/logo.png" alt="logo">
               <h2>Vuexy</h2>
             </router-link>
            </li>
           <li class="nav-adjust">
             <a href=""><span class="material-icons-outlined">adjust</span></a>   
           </li>
           <li class="close-nav"><button class="closebtn" @click="closeMenu">&times;</button></li>
         </ul>
       </div>
       <div class="navbar-container">
         <ul>
           <li class="dashboard"><a href=""><span class="material-icons-outlined">home</span><span>Dashboards</span></a></li>
           <li>
             <ul>
              <li><span class="sideListTitle">APPS &amp; PAGES</span></li>
              <li><a href=""><span class="material-icons-outlined">mail_outline</span><span>Email</span></a></li>
              <li><a href=""><span class="material-icons-outlined">chat_bubble_outline</span><span>Chat</span></a></li>
              <li><a href=""><span class="material-icons-outlined">check_box</span><span>ToDo</span></a></li>
              <li><a href=""><span class="material-icons-outlined">calendar_today</span><span>Calender</span></a></li>
              <li><a href=""><span class="material-icons-outlined">description</span><span>Invoice</span></a></li>
              <li>
                <button v-on:click="isHidden = !isHidden">
                  <a><span class="material-icons-outlined">shopping_cart</span><span>eCommerce</span></a>
                  <ul class="sub-menu" v-if="!isHidden">
                    <li><a href=""><span class="material-icons-outlined">fiber_manual_record</span><span>Shop</span></a></li>
                    <li><a href=""><span class="material-icons-outlined">fiber_manual_record</span><span>Details</span></a></li>
                    <li><a href=""><span class="material-icons-outlined">fiber_manual_record</span><span>Wishlist</span></a></li>
                    <li><a href=""><span class="material-icons-outlined">fiber_manual_record</span><span>checkout</span></a></li>
                </ul>
                </button>
                
              </li>
              <li><a href=""><span class="material-icons-outlined">person_outline</span><span>User</span></a></li>
              <li><a href=""><span class="material-icons-outlined">insert_drive_file</span><span>Pages</span></a></li>
             </ul>
             <ul>
              <li><span class="sideListTitle">USER INTERFACE</span></li>
              <li><a href=""><span class="material-icons-outlined">title</span><span>Typography</span></a></li>
              <li><a href=""><span class="material-icons-outlined">opacity</span><span>Colors</span></a></li>
              <li><a href=""><span class="material-icons-outlined">visibility</span><span>Feather</span></a></li>
              <li><a href=""><span class="material-icons-outlined">credit_card</span><span>Cards</span></a></li>
              <li><a href=""><span class="material-icons-outlined">inventory_2</span><span>Components </span></a></li>
              <li><a href=""><span class="material-icons-outlined">add_circle_outline</span><span>Extensions </span></a></li>
              <li><a href=""><span class="material-icons-outlined">space_dashboard</span><span>Page Layout </span></a></li>
              </ul>
             <ul>
              <li><span class="sideListTitle">FORMS &amp; TABLES</span></li>
              <li><a href=""><span class="material-icons-outlined">bookmarks</span><span>Form Elements</span></a></li>
              <li><a href=""><span class="material-icons-outlined">bookmarks</span><span>Form Layout</span></a></li>
              <li><a href=""><span class="material-icons-outlined">view_in_ar</span><span>Form Wizard</span></a></li>
              <li><a href=""><span class="material-icons-outlined">check_circle</span><span>Form Validation</span></a></li>
              <li><a href=""><span class="material-icons-outlined">bookmarks</span><span>Form Repeater</span></a></li>
              <li><a href=""><span class="material-icons-outlined">storage</span><span>BS Table</span></a></li>
              <li><a href=""><span class="material-icons-outlined">grid_view</span><span>Good Table</span></a></li>
             </ul>
             <ul>
              <li><span class="sideListTitle">CHARTS &amp; MAPS</span></li>
              <li><a href=""><span class="material-icons-outlined">pie_chart</span><span>Charts</span></a></li>
              <li><a href=""><span class="material-icons-outlined">menu_book</span><span>Leaflet</span></a></li>
             </ul>
             <ul>
              <li><span class="sideListTitle">OTHERS</span></li>
              <li><a href=""><span class="material-icons-outlined">shield</span><span>Access Control</span></a></li>
              <li><a href=""><span class="material-icons-outlined">menu</span><span>Menu Levels</span></a></li>
              <li><a href=""><span class="material-icons-outlined">visibility_off</span><span>Disabled Menu</span></a></li>
              <li><a href=""><span class="material-icons-outlined">sports_soccer</span><span>Raise Support</span></a></li>
              <li><a href=""><span class="material-icons-outlined">file</span><span>Documentation</span></a></li>
             </ul>
            </li>
         </ul>
       </div>
     </aside>
     <div class="app-content">
       <header>
          <nav>
            <ul>
              <ul class="nav-button"><button @click="openMenu"><span class="material-icons-outlined">reorder</span></button></ul>
              <li><a href=""><span class="material-icons-outlined">calendar_today</span></a></li>
              <li><a href=""><span class="material-icons-outlined">mail_outline</span></a></li>
              <li><a href=""><span class="material-icons-outlined">chat_bubble_outline</span></a></li>
              <li><a href=""><span class="material-icons-outlined">check_box</span></a></li>
              <li><a href=""><span class="material-icons-outlined star">star_border</span></a></li>
            </ul>
            <ul>
              <li class="language"><a href=""><img src="../assets/images/download.png" alt="language"><span>English</span></a></li>
              <li><a href=""><span class="material-icons-outlined">dark_mode</span></a></li>
              <li><a href=""><span class="material-icons-outlined">search</span></a></li>
              <li><a href=""><span class="material-icons-outlined">shopping_cart</span></a></li>
              <li><a href=""><span class="material-icons-outlined">notifications</span></a></li>
              <li>
                <div class="avatar">
                  <div class="avatar-text">
                    <p>John Doe</p>
                    <span>admin</span>
                  </div>
                  <span class="avatar"><img src="../assets/images/13-small.d796bffd.png" alt="avatar"><span></span></span>
                </div>
              </li>
            </ul>
          </nav>
       </header> 
       <div class="container">
         <ShopView/>
       </div>
       <footer></footer>
     </div> 
  </div>
</template>

<script>
import ShopView from '../views/ShopView.vue'
 
 
export default {
  name: 'HomeView',
  components: {
    ShopView  
  },
  data(){
    return {
     isHidden:true,
     showMenu:false
     } 
  },
  methods:{
    openMenu(){
       this.showMenu=!this.showMenu;
        
    },
    closeMenu(){
      this.showMenu=true;
    }
  }
}
</script>
<style scoped>
  *{
    box-sizing: border-box;
    -moz-box-sizing: border-box;
    -webkit-box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
  .home{
    position: relative;
    display: grid;
    grid-template-columns:1fr 1fr 1fr;
    grid-template-rows:1fr 1fr 1fr;
  }
    
  i{
    color:#777483;
  }
   ul{
    list-style: none;   
  }
  ul li a{
    text-decoration: none;
  }
  header nav{
    display: flex;
    align-content: center;
    justify-content: space-between;
    background-color: #fff;
    position: fixed;
    width: calc(100% - 4rem - 260px);
    margin:1.3rem 2rem 0;
    padding: .8rem 1rem;
    border-radius: .248rem;
    -webkit-box-shadow: 0 4px 24px 0 rgba(34 41 47 / 10%) !important;
    box-shadow:  0 4px 24px 0 rgba(34 41 47 / 10%) !important;
    min-height: 4rem; 
    z-index: 99; 
    
  }
 header nav ul{
   display: flex;
    align-items: center;
 }
  header nav ul a{
     padding: 0 .5rem;
   }
   header nav ul li a .star{
      color: #ff9f43;
    }
   header nav ul li.language{
     padding: 0 7px;
   }
   header nav ul li.language span{
     font-size:1rem;
     font-weight: 400;
     margin-left: .5rem;
     color: #6e6b7b!important;
   }
   header nav div.avatar{
     display: flex;
     align-items:center;
     padding: 0 7px; 
     
   }
 
   header nav span.avatar{
     width: 40px;
     height: 40px;
     position: relative;
   }
   header nav span.avatar span{
    font-size: calc(11.2px);
    bottom: 0px;
    right: 0px;
    border: 1px solid #fff;
    min-height: 11px;
    min-width: 11px;
    padding: 0.25em;
    border-radius: 10em;
    position: absolute;
    line-height: 1;
    font-weight: 700;
    z-index: 3;
    background-color: #28c76f;
   }
   header nav .avatar .avatar-text{
     display: flex;
     flex-direction: column;
     align-items: flex-end;
     margin-right: .8rem;
   }
   header nav .avatar .avatar-text p{
      font-weight: 600;
      font-size: 1rem;
      color: #777483;
   }
   header nav .avatar .avatar-text span{
      font-size: smaller;
      color: #bdbbbb;
   }
   header nav img[alt="avatar"]{
     width: 100%;
     height: 100%;
     object-fit: cover;
     border-radius: 50%;
     overflow: hidden;
   }
   header nav img[alt="language"]{
     width: 22px;
     height: 14px;
   }
 header .material-icons-outlined{
   color:#6e6b7b;
   font-size: 1.2rem;
 }
  aside{
    height: 100vh;
    position: fixed;
    top: 0;
    background: #fff;
    color: #6e6b7b;
    width: 20%;
    box-shadow: 0 0 15px 0 rgb(34 41 47 / 5%);
    text-align: left;
    z-index: 100;
  }
  aside img[alt="logo"]{
    width: 36px;
    height: 24px;
  }
 
  aside .navbar-header >ul{
    display: flex;
    justify-content: space-between;
    align-items: center;
    line-height: 1.45;
    padding: 0.35rem 1rem 0.3rem 1.64rem !important;
  }
  aside .navbar-header >ul .navbar-brand{
    margin-top: 1.35rem;
  }
  aside .navbar-header >ul li:nth-child(2) a{
    margin: 1.571rem 0;
  }
  aside .navbar-header .material-icons-outlined{
    color: #7367f0;
    font-size: 1.4rem;
  } 
  aside .material-icons-outlined{
    color: #6e6b7b;
  }
  aside .navbar-header >ul li a{
    display: flex;
    align-content: flex-start;
    align-items: baseline;
  }
  aside .navbar-header >ul h2{
    padding-left: 1rem;
    color: #7367f0;
    font-weight: 600;
    letter-spacing: .01rem;
    font-size: 1.45rem;
    line-height: 1.2;
  }
 aside .navbar-container{
   height: 100%;
   overflow: scroll !important;
 }
 ::-webkit-scrollbar {
  width: 10px;
}
::-webkit-scrollbar-track {
  background-color: #eee;
  border-radius: 4px;
}
::-webkit-scrollbar-thumb {
  background:#aaa; 
  border-radius: 6px;
  height: 15px;
  transition: background-color .2s linear,width .2s ease-in-out;
  -webkit-transition: background-color .2s linear,width .2s ease-in-out;
}
::-webkit-scrollbar-thumb:hover {
  width: 10px;
}
  aside .navbar-container ul li a:hover{
    transform:translate(6px,-1px);
    transition: all .5s ease;
  }
  aside .navbar-container ul li ul li{
    display: flex;
    align-content:center ;
    
  }
  aside .navbar-container ul li:first-child{
    margin-top: .4rem;
  }
 aside .navbar-container ul li span.sideListTitle{
   margin: 2.286rem 0 0.8rem 2.2rem;
   color: #a6a4b0;
   line-height: 1.5;
   letter-spacing: .01rem;
   font-size: .9rem;
   text-transform: uppercase;
 };
  aside .navbar-container ul li ul li:hover{
    transition: transform .25s ease;
    -webkit-transform-transition:transform .25s ease;
  }
  aside .navbar-container ul li a,aside .navbar-container ul li>span:not(.sideListTitle){
    padding: 10px 15px 10px 15px;
    margin: 0 15px;
    color: #625f6e;
    
  } 
  aside .material-icons-outlined{
    margin-right: 1.1rem;
    font-size: 1.2rem;
    font-weight: 400;
  }
  aside .navbar-container ul li .sun-menu li a{
    display: flex;
    align-content: center;
    margin: 0;
    padding: 0;
  }
  aside .navbar-container ul li button{
     background: transparent;
     border: none;
     outline: navajowhite;
  }

  .app-content{
    position: absolute;
    left: 20%;
    top: 0;
    min-height: calc(100% - 3.35rem);
    width: 80%;
     
  }
  .active{
    background-color: #7367f0;
    color: #fff;
  }
  .app-content .container{
    padding: 7.75rem 2rem 0;
  }

  /*=================================side nave toggle========================*/
 
  aside .navbar-header .close-nav .closebtn{
    color: #7367f0;
    font-size: 2rem;
  }
  .nav-button button,aside .navbar-header .close-nav .closebtn{
     outline: none;
     border: none;
     background-color: transparent;
   }
 @media only screen and (max-width: 1199px) {
   .app-content{
     width: 100%;
     left: 0;
   }

   aside .navbar-header .close-nav{
     display: block;
   }
  
   aside .nav-adjust{
     display: none;
   }
   .app-content .nav-button{
     display: block;
   }
   header nav{
     width: 94%;
   }
 }
@media only screen and (min-width: 1199px) {
   aside .navbar-header .close-nav{
     display: none;
   }
    .app-content .nav-button{
     display:none;
   }
 
}
@media only screen and (max-width: 992px){
  header nav ul:nth-child(1) li{
    display: none;
  }
}
</style>