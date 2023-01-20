<script>
export default {
  data(){
    return{
      restaurantsAddress: [
        {
          street: "1614 E. Bell RD #104",
          city: "Salerno, AZ 85022",
          phoneNumber: "(602) 867-1010"
        },
        {
          street: "204 E. Pizzeria Tommaso",
          city: "Salerno, AZ 85022",
          phoneNumber: "(602) 867-1010"
        },
        {
          street: "Via Pusglia 54",
          city: "Torre del Greco AZ 85022",
          phoneNumber: "(602) 867-1010"
        },
        {
          street: "1614 E. Bell RD #104",
          city: "Naples, AZ 85022",
          phoneNumber: "(602) 867-1010"
        }
      ],
    }
  }
}
</script>

<template>
  <footer class="row">
    <section id="general-info" class="col-lg-6 position-relative">
      <div class="row">
        <div class="col-lg-4 pe-0">
          <h3 class="fs-5 fw-bolder">FIND OUR RESTAURANTS</h3>  
          <ul class="ps-0">
            <li v-for="address in restaurantsAddress" class="list-group-item">
              <div>{{ address.street }}</div>
              <div>{{ address.city }}</div>
              <address>{{ address.phoneNumber }}</address>
            </li>
          </ul>
        </div>
        
        <div class="col-lg-4 pe-0">
          <h3 class="fs-5 fw-bolder">WORKING HOURS</h3>  
          <ul class="ps-0">
            <li class="list-group-item mb-3">
              <h4 class="mb-0">MONDAY</h4>
              <div class="red-orange">Kitchen Closed</div>
            </li>
            <li class="list-group-item mb-3">
              <h4 class="mb-0">TUSEDAY UNTIL FRIDAY</h4>
              <div>9.00 - 22.00</div>
            </li>
            <li class="list-group-item mb-3">
              <h4 class="mb-0">SATURDAY<span class="red-orange">*</span></h4>
              <div>Saturday 11am to midnight</div>
            </li>
            <li class="list-group-item mb-3">
              <h4 class="mb-0">SUNDAY</h4>
              <div>9.00 - 22.00</div>
            </li>
          </ul>
          <h4>FOLLOW US: </h4>
        </div>
        
        <div class="col-lg-4 pe-0">
          <div class="fs-3 lh-1 text-white">THE DON PEPPE CREW FIRST AND FOREMOST VALUE AN AUTHENTIC, WLL BAKED SLICE OF PIZZA.</div>
        </div>
      </div>

      <div class="position-absolute">Created with &hearts; by <span>Qode Interactive</span></div>
      <img class="position-absolute" src="https://donpeppe.qodeinteractive.com/wp-content/uploads/2019/10/footer-bottom-img.png" alt="">
    </section>
    <section class="col-lg-6 ps-0">
      <img class="img-fluid" src="../assets/img/footer-img-1.jpg" alt="people">
    </section>
  </footer>
</template>

<style lang="scss" scoped>
  @use "../style/partials/variables" as *;
  
  section#general-info{
    background-image: url(../assets/img/bg-header.png);
    padding: 90px 70px;
    color: $footer-gray;
    h3,
    h4{
      color: $gold;

    }
    h4{
      font-size: 1rem;
      font-weight: bold;

    }
    .red-orange{
      color: $red-orange;
    }
    div.position-absolute{
      bottom: 60px;
      color: $gold;
      span{
        color: $green;
      }
    }
    img.position-absolute{
      bottom: 60px;
      right: 80px;
    }
  }
</style>