

<template>
    <section class="col-12 col-md-6 col-lg-4" >
              <div class="card shadow border-0 h-100">
                  
                    <img :src="blog.image" class="card-img-top" alt="...">
                    
                  <div class="card-body d-flex flex-column" >
                    <h5 class="card-title fw-bold lh-base"> {{blog.subject}}</h5>
                    <p class="card-text">{{blog.subtitle}}</p>
                    <div class="mt-auto">
                      <div class="star-rating">
                        <i class="far fa-star"></i><i class="far fa-star"></i><i class="far fa-star"></i><i class="far fa-star"></i><i class="far fa-star"></i>
                        <!--(จำนวนคะแนน / 5 ดาว)*100 = x% -->
                        <div class="star-current" style="width: 50%;">
                          <i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i>
                        </div>
                      </div>
                      <small class="text-muted">4.5(50)</small>
                      <small class="float-end"><i class="fas fa-eye"></i>{{blog.view}}</small>
                      <div class="d-grid  mt-2">
                        <a href="blog-detail.html" class="btn btn-primary">
                          READ MORE <i class="fas fa-arrow-circle-right"></i>
                        </a>
                      </div>
                    
                    </div>
                  </div>
                </div>
              </section>
</template>
 
<script>
module.exports = {
    props:['blog']
}
</script>
 
<style >

</style>