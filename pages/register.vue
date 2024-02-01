<template>
            <div class="form">
                <div class="formcontent">
                    <h1>Register <span>Now</span></h1>
                    <input type="text" placeholder="Username">
                    <input type="email" placeholder="Email">
                    <button class="btn">Submit</button>
                </div>
            </div>
</template>
<style>
.form {
  width: 440px;
  height: 310px;
  margin: 100px auto;
  padding: 40px;
  background-color: var(--secondary);
  box-shadow: 0 0 20px rgba(0,0,0,0.1);
  text-align: center;
  border-radius: 5%;
}
.btn
{
    margin-top: 10px;
      border: none;
      padding: 10px 30px;
      background: #fff;
      border-radius: 25px;
      cursor: pointer;
      transition: .5s;
}

.form .formcontent
{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    gap: 10px;
}
.form .formcontent input
{
    border: none;
    padding: 10px 30px;
    border-radius: 20px;
}
</style>