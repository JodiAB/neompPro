<template>
  <div class="about desire">
    <h1 class="header">About Us</h1>
    <br>
   
    <p class="para" id="special1">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quae, in ea? Eligendi dolore, quisquam neque ab laborum dolores voluptate doloribus maxime praesentium mollitia nisi magnam dignissimos? Esse, sit debitis quo blanditiis dolor accusantium magni saepe repellat exercitationem iste dolore, odit suscipit fugit fuga dolorem est, illo cupiditate quibusdam. Tempore iure nobis sequi unde voluptate consequuntur a sed molestiae voluptatum neque? In doloribus rem facilis nihil non saepe reprehenderit suscipit nisi. Non facere, nemo obcaecati doloribus qui velit magni dolorem consequuntur! Delectus debitis totam iste ab amet officiis illum, distinctio laborum architecto dolore a rerum laboriosam adipisci sapiente officia quia veniam?</p>


    <div class="banner animated tada">
      <div class=" big-text animated tada">95% OFF</div>
       <div>the entire store</div>
       <a href="#">Go to store</a>
     </div>
</div>
</template>
<style>
.about{
 
  height: 200vh;
  max-width: 100%;
  border: 2px solid white;

}
.desire{
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 100%;
  height: 110vh;
  background: linear-gradient(-50deg, rgb(48, 47, 47), #191a19, rgb(136, 135, 135), #666565);
  background-size: 200% 200%; 
  animation: fire 7s ease infinite;

}

@keyframes fire {
  0%{
  background-position: 0% 50%;
}
50%{
  background-position: 100% 50%;
}
100%{
  background-position: 0% 50%;
}
}
.header{
  display:flex;
  color:black;
  font-size: 40px;
  justify-content: center;
}
 .para{
  color: aliceblue;
  /* text-align: center; */
  display: flex;
  justify-content: center;
  /* align-items: center; */
  border: 3px solid black;
  border-radius: 20px;
  font-size: 20px;
  width: 278px;
  margin-left: 70px;
  background: linear-gradient(100deg, #f5e3df 20%, #FFC300,#4c4b4b);
  -webkit-background-clip: text;
  background-clip: text;
  -webkit-text-fill-color: transparent;
  animation: gradientAnimation 0.5s linear infinite alternate;
  background-size: 200% 100%;
  text-shadow: 0px 0px 10px rgba(255, 255, 255, 0.5);

}

.banner {
  width: 100%;
  background:url(http://s6.favim.com/orig/150112/background-cold-gif-nature-Favim.com-2380226.gif);
  /*https://i0.wp.com/media.giphy.com/media/5ERaOy5fQEIAU/giphy.gif*/
  background-size: cover;
  font-size: 80px;
  color: #fff;
  text-align: center;
  padding: 40px 15px;
  height: 100vh;
}

.big-text {
  font-size: 130px;
  font-weight:800;
  animation-delay: 1s;
}
.banner a {
  display: inline-block;
  background: #fff;
  color: #36465d;
  text-transform: uppercase;
  padding: 15px;
  text-decoration: none;
  font-size: 40px;
  transition: .3s;
}
.banner a:hover {
  background: #333;
  color: #fff;
  padding: 15px 20px;
}
</style>
