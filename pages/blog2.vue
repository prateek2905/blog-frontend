<template>

    <div class="background">
      <div class="content">        
        <div class="main-content">
          <div class="left-para">
            <div class="introTitle">
              Innovating Artificial Intelligence
            </div>
            <p>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer nisi magna, rutrum ut justo sed, congue semper magna. Sed suscipit aliquam dolor efficitur convallis. Pellentesque vitae nibh in mi lobortis euismod. Duis odio lacus, gravida vel velit et, bibendum tristique justo. Nam vitae lorem ut dolor consequat commodo sit amet id enim. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum vitae sapien lorem. Quisque non eros ut dui ornare euismod. Mauris nulla eros, tincidunt eu mi in, molestie mattis urna. Sed eu interdum leo, at lobortis nulla. Praesent fermentum urna sit amet fermentum imperdiet. In eu maximus metus, accumsan tempor est. Nullam ac tortor ante. Praesent elementum ut elit ut tincidunt.
            </p>
            <br/>
            <p>Written by- User 7</p>
            </div>         
          <div class="main-content-image"></div>
        </div> 
      </div>
    </div>

</template>
  
  
  <style lang="css">

  .main-content-image {
    background-image: url("https://i.postimg.cc/gkCk3bbx/pexels-cottonbro-studio-3944425.jpg");
    border-radius: 8px;
    background-position: center center;
    background-size: cover;
    box-shadow: 0 1px 2px #0000000d, 0 4px 8px #0000000d;
    flex: 0.5;
  }
  .introTitle {
    font-size: 2rem;
    font-weight: 700;
    line-height: 2.5rem;
    margin-bottom: 2rem;
  }
  .background {
    border: 5px solid rgb(0, 0, 0);
    background-color: white;
    border-radius: 15px;
    margin: 40px 200px;
    padding: 34px;
  }

  .main-content { 
    display: flex;
    width: 100%;
    flex-flow: row wrap;
  }
  .main-content .left-para {
    margin-right: 45px;
    text-align: start;
    flex: 0.5;
  }
  .main-content .left-para h2 {
    font-size: 2rem;
    margin-bottom: 50px;
  }
  </style>
  