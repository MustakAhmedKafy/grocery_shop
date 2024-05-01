<script setup>
const logo = "./img/logo.png";
</script>
<template>
  <footer class="py-5 text-center">
    <div class="container">
      <div class="row">
        <div class="col-lg-2 col-md-2 col-6 mb-3">
          <img class="w-50" :src="logo" alt="" />
          <p>Camford Way</p>
          <p>Luton</p>
          <p>Bedfordshire</p>
          <p>LU3 3AN</p>
          <p>+880124122222</p>
        </div>
        <div class="col-lg-2 col-md-2 col-6 mb-3">
          <h6><b>Company</b></h6>
          <p><a href="">Promotions</a></p>
          <p><a href="">FAQs</a></p>
          <p><a href="">Contact Us</a></p>
        </div>
        <div class="col-lg-2 col-md-2 col-6 mb-3">
          <h6><b>General</b></h6>
          <p><a href="">Terms & Conditions</a></p>
          <p><a href="">Privacy Policy</a></p>
          <p><a href="">Opening Times</a></p>
          <p><a href="">Find Us</a></p>
        </div>
        <div class="col-lg-2 col-md-2 col-6 mb-3">
          <h6><b>Features</b></h6>
          <p><a href="">Hospitality Features</a></p>
          <p><a href="">Management</a></p>
          <p><a href="">Security</a></p>
          <p><a href="">Payments</a></p>
          <p><a href="">Advanced Reporting</a></p>
        </div>
        <div class="col-lg-2 col-md-2 col-6 mb-3">
          <h6><b>Timings</b></h6>
          <p>Monday - Friday (9AM to 10PM)</p>
          <p>Saturday - Sunday (9AM to 5PM)</p>
        </div>

        <div class="col-lg-2 col-md-2 col-6 mb-3">
          <h6><b>Customer service</b></h6>
          <p>Monday - Sunday</p>
          <p><a href="">+01582 599929</a></p>
          <p><a href="">info@msfoods.co.uk</a></p>
          <div class="social-icon">
            <ul>
              <li><i class="fa-brands fa-twitter"></i></li>
              <li><i class="fa-brands fa-facebook"></i></li>
              <li><i class="fa-brands fa-youtube"></i></li>
              <li><i class="fa-brands fa-instagram"></i></li>
            </ul>
          </div>
        </div>
        <hr />
        <p class="pt-3 copyright">
          Mustak Ahmed © 2024 • Privacy Policy • Cookie Policy
        </p>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
$primary-color: #577537;
$secondary-color: red;
footer {
  a {
    text-decoration: none;
  }

  p {
    font-size: 13px;
    opacity: 0.9;
    margin: 0;
    padding-bottom: 5px;
    color: #000;
  }

  a {
    color: #000;
    font-weight: 500;
    opacity: 0.9;

    &:hover {
      color: $primary-color;
    }
  }

  ul {
    padding: 0;

    li {
      display: inline;
      text-align: left;
      padding-right: 5px;
      transition: 0.7s;

      &:hover {
        color: $primary-color;
        transition: 0.7s;
      }
    }
  }

  .copyright {
    color: gray;
    text-align: center;
  }
}
</style>
