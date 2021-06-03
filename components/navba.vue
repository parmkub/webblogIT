<template>
    <nav class="navbar navbar-expand-md ">
          <div class="container">
            <a class="navbar-brand" href="#">
              <img src="assets/images/text_logo.png" height="50px" alt="" />
            </a>
            <button
              class="navbar-toggler"
              type="button"
              data-bs-toggle="collapse"
              data-bs-target="#navbarContent"
              aria-controls="navbarContent"
              aria-expanded="false"
              aria-label="Toggle navigation"
            >
              <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarContent">
              <ul class="navbar-nav ms-auto float-end ul-navbar">
                <li class="nav-item px-3 px-md-0 active">
                  <a class="nav-link" href="#">IT Blog</a>
                </li>
                <li class="nav-item px-3 px-md-0">
                  <a class="nav-link" href="register.html">สมัครสมาชิก</a>
                </li>
                <li class="nav-item px-3 px-md-0">
                  <a class="nav-link" href="login.html">เข้าสู่ระบบ</a>
                </li>
                <li class="nav-item px-3 dropdown">
                    <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-bs-toggle="dropdown" aria-expanded="false">
                      <img src="assets/images/Uploads/avatar.png" width="40px" height="40px" alt="" class="profile-img">
                      FirstName
                    </a>
                    <ul class="dropdown-menu dropdown-menu-end mb-3" aria-labelledby="navbarDropdown">
                      <li>
                        <a class="dropdown-item" href="profile.html">
                          <div class="d-flex align-items-center">
                            <img src="assets/images/Uploads/avatar.png" width="40px" height="40px" alt="" class="profile-img">
                            <div class="lh-sm p-3">
                              <span class="font-weigh-bold">FirstName Lasname</span><br>
                              <small>ดูโปรไฟล์ของคุณ</small>
                            </div>
                            
                          </div>
                        </a>
                    </li>
                      <li><a class="dropdown-item" href="#">ออกจากระบบ</a></li>
                    </ul>
                </li>
              </ul>
            </div>
          </div>
          <div class="progressContainer">
            <div class="progressBar">

            </div>

        </div>
        </nav>
        
</template>
 
<script>
module.exports = {
  
    mounted(){
        window.addEventListener('scroll',function(){
            let wintop = this.scrollY
            let navbar = document.querySelector(".navbar")

            let winheight = this.innerHeight
            //console.log(winheight)
            let docheight = document.querySelector("body").offsetHeight
            let bar = document.querySelector(".progressBar")
            let totalScroll = (wintop / (docheight - winheight))*100
            bar.style.width = `${totalScroll}%`

            navbar.classList.add("navbar-light", "fixed-top", "bg-light")
            if(wintop >150){
              //console.log('เปลียนพื้นหลังเป็นสีขาว')
              //navbar-light bg-light
              //navbar-dark  bg-transaparent
              navbar.classList.remove("navbar-dark","bg-transaparent")
              navbar.classList.add("navbar-light","bg-light")
              
            }else{
              //console.log('เปลียนพื้นหลังเป็นโปร่งใส')
              navbar.classList.remove("navbar-light","bg-light")
              navbar.classList.add("navbar-dark","bg-transaparent")
              
             
            }

        })
    }
   
}

// mounted() ในเหตุกาณณ์นี้ จะเกิดขึ้น DOM ถูกสร้างเสร็จแล้ว ราสามารถเข้าถึง Element ต่างใน DOM ได้ทั้งหมด
</script>
 


<style></style>