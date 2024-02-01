<template>
  <body>
    
    <div class="top">
        <div class="head">
            Blog<span>Works</span>
        </div>        
    </div>
    
    <div class="header">
        <ul class="navigation">
            <li><a href="#top">HOME</a></li>
            <li><a href="#news">NEWS BLOGS</a></li>
            <li><a href="#latest">LATEST BLOGS</a></li>
            <li><NuxtLink to="/register">REGISTER</NuxtLink></li>
        </ul>
    </div>
    
    <!--NEWS SECTION-->
    <section class="news" id="news">
        <div class="titletext">
            <h1>News <span>Blogs</span></h1>
        </div>
        <div class="container">
            <div class="card" v-for="item in items" :key="item.title">
              <div class="card__header">
                <img :src="item.image" alt="card__image" class="card__image" width="600">
              </div>
              <div class="card__body">
                <NuxtLink :to="item.link"><h4>{{ item.title }}</h4></NuxtLink>
                <p>{{ item.message }}</p>
              </div>
              <div class="card__footer">
                <div class="user">
                  <div class="user__info">
                    <h5>Written by-{{ item.user }}</h5>
                    <small>{{ item.time }}</small>
                  </div>
                </div>
              </div>
            </div>           
        </div>
    </section>

    <!--LATEST SECTION-->
    <section class="news" id="latest">
        <div class="titletext">
            <h1>Latest <span>Blogs</span></h1>
        </div>
        <div class="container">
            <div class="card" v-for="blog in blogs" :key="blog.title">
              <div class="card__header">
                <img :src="blog.image" alt="card__image" class="card__image" width="600">
              </div>
              <div class="card__body">
                <NuxtLink :to="blog.link"><h4>{{ blog.title }}</h4></NuxtLink>
                <p>{{ blog.message }}</p>
              </div>
              <div class="card__footer">
                <div class="user">
                  <div class="user__info">
                    <h5>{{ blog.user }}</h5>
                    <small>{{ blog.time }}</small>
                  </div>
                </div>
              </div>
            </div>           
        </div>
    </section>
    
  </body>
</template>
  
  <style>
    @import url("https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600&display=swap");
  :root {
      --primary: #111;
      --secondary: #59b2de;
      --bg: #F0F8FF;
      --border: #aaa;
  }
  *
  {
      box-sizing: border-box;
      padding: 0;
      margin: 0;
      font-family: 'Poppins', sans-serif;
      scroll-behavior: smooth ;
  }
  .top
  {
      display: flex;
      justify-content: space-between;
      align-items: center;
      height: 80px;
      width: 100%;
      padding: 0 50px;
      font-size: 1.5em;
      font-weight: 600;
  }
  .top span
  {
    color: var(--secondary)
  }
  
  .header
  {
      height: 60px;
      width: 100%;
      display: flex;
      justify-content: center;
      align-items: center;
      border-top: 1px solid var(--border);
      border-bottom: 1px solid var(--border);
      position: sticky;
      top: 0;
      z-index: 1000;
      background: #fff;
  }
  .header .navigation
  {
      display: flex;
      justify-content: center;
      align-items: center;
      list-style: none;
      position: relative;
  }
  .header .navigation li a
  {
      text-decoration: none;
      color: var(--primary);
      padding: 5px 40px;
      transition: .3s ease-in-out;
  }
  .header .navigation li a:hover
  {
      color: var(--secondary);
  }
 
  section
    {
      padding: 40px 30px;
    }
  
  .container {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      margin-block: 2rem;
      gap: 2rem;
      background: var(--bg);
      border-radius: 20px;
      padding: 50px 0px;
    }
    
    img {
      max-width: 100%;
      object-fit: cover;
    }
    
    .card {
      display: flex;
      flex-direction: column;
      align-items: center;
      width: clamp(20rem, calc(20rem + 2vw), 22rem);
      overflow: hidden;
      box-shadow: 0 .1rem 1rem rgba(0, 0, 0, 0.1);
      border-radius: 1em;
      background: #fff;
      color: var(--primary);
    }
    
    .card__body {
      padding: 1rem;
      display: flex;
      flex-direction: column;
      gap: .5rem;
    }
    
    .card__body h4 {
      font-size: 1.5rem;
      color: var(--primary);
    }
    
    .card__footer {
      display: flex;
      padding: 1rem;
      margin-top: auto;
    }
    
  .news
  {
      text-align: center;
  }
  .news .titletext
  {
      text-align: center;
      font-size: 2em;
      padding-bottom: 40px;
  }
  .news .titletext span
  {
      color: var(--secondary);
  }

  </style>
  
  <script>
  export default {
    data(){
      return{
        items: [
        {
            title: "Latest Tech Products",
            image:"https://i.postimg.cc/gkCk3bbx/pexels-cottonbro-studio-3944425.jpg",
            message:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Sequi perferendis molestiae non nemo doloribus. Doloremque, nihil! At ea atque quidem!",
            user: "user 3",
            time: "2h ago",
            link: "/blog1"
          },
          {
            title: "Innovating Artificial Intelligence",
            image:"https://i.postimg.cc/x1LjRp9t/pexels-cottonbro-studio-3944454.jpg",
            message:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Sequi perferendis molestiae non nemo doloribus. Doloremque, nihil! At ea atque quidem!",
            user: "user 7",
            time: "30 mins ago",
            link: "/blog2"
          },
          {
            title: "Stock Market Analysis",
            image:"https://images.pexels.com/photos/2774556/pexels-photo-2774556.jpeg?auto=compress&cs=tinysrgb&w=600",
            message:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Sequi perferendis molestiae non nemo doloribus. Doloremque, nihil! At ea atque quidem!",
            user: "user 5",
            time: "4h ago",
            link: "/blog3"
          },
          {
            title: "Marketing Techniques",
            image:"https://images.pexels.com/photos/2774556/pexels-photo-2774556.jpeg?auto=compress&cs=tinysrgb&w=600",
            message:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Sequi perferendis molestiae non nemo doloribus. Doloremque, nihil! At ea atque quidem!",
            user: "user 1",
            time: "2 days ago",
            link: "/blog3"
          },
          {
            title: "New in 2024",
            image:"https://i.postimg.cc/J7dh4BTc/pexels-cottonbro-studio-3944460.jpg",
            message:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Sequi perferendis molestiae non nemo doloribus. Doloremque, nihil! At ea atque quidem!",
            user: "user 1",
            time: "recently",
            link: "/blog1"
          },
          {
            title: "Trends in IT",
            image:"https://images.pexels.com/photos/919734/pexels-photo-919734.jpeg?auto=compress&cs=tinysrgb&w=600",
            message:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Sequi perferendis molestiae non nemo doloribus. Doloremque, nihil! At ea atque quidem!",
            user: "user 1",
            time: "1h ago",
            link: "/blog2"
          },
        ],
        blogs: [
          {
            title: "Conference meeting",
            image:"https://images.pexels.com/photos/2774556/pexels-photo-2774556.jpeg?auto=compress&cs=tinysrgb&w=600",
            message:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Sequi perferendis molestiae non nemo doloribus. Doloremque, nihil! At ea atque quidem!",
            user: "user 1",
            time: "2h ago",
            link: "/blog3"
          },
          {
            title: "Motivational Talks",
            image:"https://images.pexels.com/photos/2774572/pexels-photo-2774572.jpeg?auto=compress&cs=tinysrgb&w=600&lazy=load",
            message:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Sequi perferendis molestiae non nemo doloribus. Doloremque, nihil! At ea atque quidem!",
            user: "user 2",
            time: "2h ago",
            link: "/blog2"
          },
          {
            title: "How to DJ",
            image:"https://images.pexels.com/photos/919734/pexels-photo-919734.jpeg?auto=compress&cs=tinysrgb&w=600",
            message:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Sequi perferendis molestiae non nemo doloribus. Doloremque, nihil! At ea atque quidem!",
            user: "user 3",
            time: "4h ago",
            link: "/blog1"
          }
        ]
      }
    }
  }
  </script>
  