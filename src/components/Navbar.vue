<script setup>
import { ref } from "vue";
import NavCart from "./reusable/NavCart.vue";

const showCart = ref(false);

const toggleCart = () => {
  showCart.value = !showCart.value;
  console.log("showCart value:", showCart.value);
};

function handleClickOutside(event) {
  if (!event.target.closest(".header-cart")) {
    showCart.value = false; // Change isCartOpen to showCart
  }
}

function closeCart() {
  showCart.value = false;
}

const logo = "./img/logo.png";
const fruit1 = "./img/fruits-1.jpg";
const fruit2 = "./img/fruits-2.jpg";
const fruit3 = "./img/fruits-3.jpg";
const fruit4 = "./img/fruits-4.jpg";
const fruit5 = "./img/fruits-5.jpg";
const fruit6 = "./img/fruits-6.jpg";
const fruit7 = "./img/fruits-7.jpg";
const fruit8 = "./img/fruits-8.jpg";
const discountImage = "./img/tastydaily-0455830109.jpg";

const socialMedia = [
  { icon: "fa-facebook-f", link: "#" },
  { icon: "fa-instagram", link: "#" },
  { icon: "fa-whatsapp", link: "#" },
  { icon: "fa-youtube", link: "#" },
];

// click dropdown stop
const toggleDropdown = (event) => {
  const dropdown = event.target.nextElementSibling;
  dropdown.classList.toggle("show");
};

// hover dropdown
const dropdowns = document.querySelectorAll(".dropdown");
dropdowns.forEach((element) => {
  const dropdownItem = element.querySelector(".dropdown-menu");
  element.addEventListener("mouseover", function () {
    dropdownItem.classList.add("show");
  });
  element.addEventListener("mouseout", function () {
    dropdownItem.classList.remove("show");
  });
});
</script>

<template>
  <section class="header-top d-none d-lg-block py-3">
    <div class="container">
      <div class="d-flex justify-content-between">
        <div>
          <span
            ><i class="fa-regular fa-clock"></i> Delivery on Next Day from 10:00
            AM to 08:00 PM</span
          >
        </div>

        <div class="header-social">
          <span
            ><i class="fa-solid fa-headphones-simple"></i> +880-171604506</span
          >
          <div class="social d-inline">
            <span v-for="media in socialMedia" :key="media.icon">
              <i
                :class="['fa-brands', media.icon]"
                :aria-label="media.icon"
              ></i>
            </span>
          </div>
        </div>
      </div>
    </div>
  </section>
  <header>
    <nav class="navbar navbar-expand-lg shadow">
      <div class="container">
        <a class="navbar-brand" href="#"><img :src="logo" alt="" /></a>
        <button
          class="navbar-toggler collapsed"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbar-content"
        >
          adadasd
        </button>
        <div class="collapse navbar-collapse" id="navbar-content">
          <!-- mega menu start-->
          <ul class="navbar-nav mx-auto mb-2 mb-lg-0">
            <li class="nav-item dropdown dropdown-mega position-static">
              <a
                class="nav-link dropdown-toggle"
                href="#"
                data-bs-toggle="dropdown"
                data-bs-auto-close="outside"
                @click="toggleDropdown"
              >
                Shop</a
              >
              <div class="dropdown-menu mega-dropdown shadow">
                <div class="mega-content px-4">
                  <div class="container-fluid">
                    <div class="row">
                      <div class="col-12 col-lg-3 col-md-6 py-4">
                        <h5>Dairy</h5>
                        <p>Whole Milk</p>
                        <p>2% Reduced Fat</p>
                        <p>Skim Milk</p>
                        <p>Almond Milk</p>
                        <p>Parmesan</p>
                        <h5>Fresh Produce</h5>
                        <p>Apples</p>
                        <p>Bananas</p>
                        <p>Oranges</p>
                        <p>Berries</p>
                        <p>Grapes</p>
                      </div>
                      <div class="col-12 col-lg-3 col-md-6 py-4">
                        <h5>Cheese</h5>
                        <p>Cheddar</p>
                        <p>Swiss</p>
                        <p>
                          Parmesan <span class="badge bg-warning">hot</span>
                        </p>
                        <p>Mozzarella</p>
                        <h5>Beef</h5>
                        <p>Ground Beef</p>
                        <p>Roast <span class="badge bg-warning">hot</span></p>
                        <p>Ground Turkey</p>
                        <p>Chicken</p>
                        <p>Steak</p>
                      </div>
                      <div class="col-12 col-lg-3 col-md-6 py-4">
                        <h5>Bread</h5>
                        <p>Whole Wheat</p>
                        <p>White <span class="badge bg-warning">hot</span></p>
                        <p>Multigrain</p>
                        <p>Sourdough</p>
                        <p>Gluten-free</p>
                        <h5>Snacks</h5>
                        <p>Potato Chips</p>
                        <p>
                          Tortilla Chips
                          <span class="badge bg-warning">hot</span>
                        </p>
                        <p>Pretzels</p>
                        <p>Popcorn</p>
                        <p>Veggie Chips</p>
                      </div>
                      <div class="col-12 col-lg-3 col-md-6 py-4">
                        <h5>Beverages</h5>
                        <p>Still Water</p>
                        <p>
                          Sparkling Water
                          <span class="badge bg-warning">hot</span>
                        </p>
                        <p>Flavored Water</p>
                        <p>Coconut Water</p>
                        <p>Sports Drinks</p>
                        <h5>Frozen Foods</h5>
                        <p>Margherita</p>
                        <p>
                          Gluten-free<span class="badge bg-warning">hot</span>
                        </p>
                        <p>Mint Chocolate Chip</p>
                        <p>Chocolate</p>
                        <p>Strawberry</p>
                        <p>Vanilla</p>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </li>
            <li class="nav-item dropdown">
              <a
                class="nav-link dropdown-toggle"
                href="#"
                data-bs-toggle="dropdown"
                data-bs-auto-close="outside"
                @click="toggleDropdown"
                >Vegetables</a
              >
              <ul class="dropdown-menu shadow">
                <li><a class="dropdown-item" href="#">Carrots</a></li>
                <li><a class="dropdown-item" href="blog.html">Broccoli</a></li>
                <li><a class="dropdown-item" href="#"> Spinach</a></li>
                <li><a class="dropdown-item" href="#"> Bell peppers</a></li>
                <li><a class="dropdown-item" href="#"> Tomatoes</a></li>
              </ul>
            </li>

            <li class="nav-item dropdown dropdown-mega position-static">
              <a
                class="nav-link dropdown-toggle"
                href="#"
                data-bs-toggle="dropdown"
                data-bs-auto-close="outside"
                @click="toggleDropdown"
                >Fresh Fruits</a
              >
              <div class="dropdown-menu mega-dropdown shadow">
                <div
                  class="mega-content text-lg-start text-md-start text-center px-4"
                >
                  <div class="container-fluid">
                    <div class="row">
                      <div class="col-12 col-lg-3 col-md-6 py-4">
                        <h5>Citrus Fruits</h5>
                        <p>Orange</p>
                        <p>Lemon</p>
                        <p>Lime</p>
                        <p>Grapefruit</p>
                        <p>Blood Orange</p>
                        <h5>Berries</h5>
                        <p>Strawberry</p>
                        <p>Blueberry</p>
                        <p>Oranges</p>
                        <p>Raspberry</p>
                        <p>Blackberry</p>
                      </div>
                      <div class="col-12 col-lg-3 col-md-6 py-4">
                        <div class="d-flex align-items-center">
                          <div class="flex-shrink-0">
                            <img
                              alt="64x64"
                              :src="fruit8"
                              data-holder-rendered="true"
                            />
                          </div>
                          <div class="flex-grow-1 ms-3">
                            <h6 class="mt-0">Avocados 2 Units</h6>
                            <div class="rating">
                              <span><i class="fa-solid fa-star"></i></span>
                              <span><i class="fa-solid fa-star"></i></span>
                              <span><i class="fa-solid fa-star"></i></span>
                              <span><i class="fa-solid fa-star"></i></span>
                              <span><i class="fa-solid fa-star"></i></span>
                              <p class="mt-2">£60.00</p>
                            </div>
                          </div>
                        </div>
                        <div class="d-flex align-items-center">
                          <div class="flex-shrink-0">
                            <img
                              alt="115x115"
                              :src="fruit1"
                              data-holder-rendered="true"
                            />
                          </div>
                          <div class="flex-grow-1 ms-3">
                            <h6 class="mt-0">Kiwi</h6>
                            <div class="rating">
                              <p class="mt-2">£60.00</p>
                            </div>
                          </div>
                        </div>
                        <div class="d-flex align-items-center">
                          <div class="flex-shrink-0">
                            <img
                              alt="115x115"
                              :src="fruit2"
                              data-holder-rendered="true"
                            />
                          </div>
                          <div class="flex-grow-1 ms-3">
                            <h6 class="mt-0">Fresh coconut 2 Units</h6>
                            <div class="rating">
                              <p class="mt-2">£60.00</p>
                            </div>
                          </div>
                        </div>
                        <div class="d-flex align-items-center">
                          <div class="flex-shrink-0">
                            <img
                              alt="115x115"
                              :src="fruit3"
                              data-holder-rendered="true"
                            />
                          </div>
                          <div class="flex-grow-1 ms-3">
                            <h6 class="mt-0">Avocados 2 Units</h6>
                            <div class="rating">
                              <span><i class="fa-solid fa-star"></i></span>
                              <span><i class="fa-solid fa-star"></i></span>
                              <span><i class="fa-solid fa-star"></i></span>
                              <span><i class="fa-solid fa-star"></i></span>
                              <span><i class="fa-solid fa-star"></i></span>
                              <p class="mt-2">£60.00</p>
                            </div>
                          </div>
                        </div>
                      </div>
                      <div class="col-12 col-lg-3 col-md-6 py-4">
                        <div class="d-flex align-items-center">
                          <div class="flex-shrink-0">
                            <img
                              alt="115x115"
                              :src="fruit4"
                              data-holder-rendered="true"
                            />
                          </div>
                          <div class="flex-grow-1 ms-3">
                            <h6 class="mt-0">Grapes 1 Units</h6>
                            <div class="rating">
                              <span><i class="fa-solid fa-star"></i></span>
                              <span><i class="fa-solid fa-star"></i></span>
                              <span><i class="fa-solid fa-star"></i></span>
                              <span><i class="fa-solid fa-star"></i></span>
                              <span><i class="fa-solid fa-star"></i></span>
                              <p class="mt-2">£60.00</p>
                            </div>
                          </div>
                        </div>
                        <div class="d-flex align-items-center">
                          <div class="flex-shrink-0">
                            <img
                              alt="115x115"
                              :src="fruit5"
                              data-holder-rendered="true"
                            />
                          </div>
                          <div class="flex-grow-1 ms-3">
                            <h6 class="mt-0">Orange 2 Units</h6>
                            <div class="rating">
                              <p class="mt-2">£60.00</p>
                            </div>
                          </div>
                        </div>
                        <div class="d-flex align-items-center">
                          <div class="flex-shrink-0">
                            <img
                              alt="115x115"
                              :src="fruit6"
                              data-holder-rendered="true"
                            />
                          </div>
                          <div class="flex-grow-1 ms-3">
                            <h6 class="mt-0">watermalon 5 Units</h6>
                            <div class="rating">
                              <p class="mt-2">£60.00</p>
                            </div>
                          </div>
                        </div>
                        <div class="d-flex align-items-center">
                          <div class="flex-shrink-0">
                            <img
                              alt="115x115"
                              :src="fruit7"
                              data-holder-rendered="true"
                            />
                          </div>
                          <div class="flex-grow-1 ms-3">
                            <h6 class="mt-0">Apple 2 Units</h6>
                            <div class="rating">
                              <span><i class="fa-solid fa-star"></i></span>
                              <span><i class="fa-solid fa-star"></i></span>
                              <span><i class="fa-solid fa-star"></i></span>
                              <span><i class="fa-solid fa-star"></i></span>
                              <span><i class="fa-solid fa-star"></i></span>
                              <p class="mt-2">£60.00</p>
                            </div>
                          </div>
                        </div>
                      </div>
                      <div class="col-12 col-lg-3 col-md-6 py-4">
                        <div class="header-big-sale-img">
                          <h2>Big Sale for Strawberries!</h2>
                          <p class="display-5 fw-bold">-50%</p>
                          <button class="btn btn-primary rounded-pill">
                            Shop now
                          </button>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </li>
            <li class="nav-item dropdown">
              <a
                class="nav-link dropdown-toggle"
                href="#"
                data-bs-toggle="dropdown"
                data-bs-auto-close="outside"
                @click="toggleDropdown"
                >Meat</a
              >
              <ul class="dropdown-menu shadow">
                <li><a class="dropdown-item" href="#">Halal Chicken</a></li>
                <li><a class="dropdown-item" href="blog.html">Lamb</a></li>
                <li><a class="dropdown-item" href="#"> Beef</a></li>
                <li><a class="dropdown-item" href="#"> Goat</a></li>
                <li><a class="dropdown-item" href="#"> Turkey</a></li>
              </ul>
            </li>
            <li class="nav-item dropdown">
              <a
                class="nav-link dropdown-toggle"
                href="#"
                data-bs-toggle="dropdown"
                data-bs-auto-close="outside"
                @click="toggleDropdown"
                >Seafood</a
              >
              <ul class="dropdown-menu shadow">
                <li><a class="dropdown-item" href="#">Salmon</a></li>
                <li><a class="dropdown-item" href="blog.html">Shrimp</a></li>
                <li><a class="dropdown-item" href="#"> Tuna</a></li>
                <li><a class="dropdown-item" href="#"> Cod</a></li>
                <li><a class="dropdown-item" href="#"> Lobster</a></li>
              </ul>
            </li>
            <li class="nav-item dropdown">
              <a
                class="nav-link dropdown-toggle"
                href="#"
                data-bs-toggle="dropdown"
                data-bs-auto-close="outside"
                @click="toggleDropdown"
                >Baking</a
              >
              <ul class="dropdown-menu shadow">
                <li><a class="dropdown-item" href="#">Cupcakes</a></li>
                <li><a class="dropdown-item" href="blog.html">Brownies</a></li>
                <li><a class="dropdown-item" href="#"> Bagels</a></li>
                <li><a class="dropdown-item" href="#"> Scones</a></li>
                <li><a class="dropdown-item" href="#"> Biscuits</a></li>
              </ul>
            </li>
            <li class="nav-item dropdown">
              <a
                class="nav-link dropdown-toggle"
                href="#"
                data-bs-toggle="dropdown"
                data-bs-auto-close="outside"
                @click="toggleDropdown"
                >Drinks</a
              >
              <ul class="dropdown-menu shadow">
                <li>
                  <a class="dropdown-item" href="#">RefreshRite Beverages</a>
                </li>
                <li>
                  <a class="dropdown-item" href="blog.html"
                    >QuenchCraft Drinks</a
                  >
                </li>
                <li>
                  <a class="dropdown-item" href="#"> ThirstBuster Selections</a>
                </li>
                <li><a class="dropdown-item" href="#"> Hydrate Haven</a></li>
                <li>
                  <a class="dropdown-item" href="#"> Sip & Shop Elixirs</a>
                </li>
                <li>
                  <a class="dropdown-item" href="#"> Sip & Shop Elixirs</a>
                </li>
              </ul>
            </li>
            <li class="nav-item dropdown">
              <a
                class="nav-link dropdown-toggle"
                href="#"
                data-bs-toggle="dropdown"
                data-bs-auto-close="outside"
                @click="toggleDropdown"
                >Others</a
              >
              <ul class="dropdown-menu shadow">
                <li>
                  <a class="dropdown-item" href="#">Household Cleaners</a>
                </li>
                <li>
                  <a class="dropdown-item" href="blog.html"
                    >Personal Care Products</a
                  >
                </li>
                <li>
                  <a class="dropdown-item" href="#"> Canned Goods</a>
                </li>
                <li>
                  <a class="dropdown-item" href="#"> Breakfast Cereals</a>
                </li>
                <li>
                  <a class="dropdown-item" href="#"> Snack Items</a>
                </li>
              </ul>
            </li>
          </ul>
          <!-- mega menu end-->

          <div class="d-flex align-items-center">
            <div class="d-inline">
              <div class="input-group">
                <input
                  type="text"
                  class="form-control"
                  aria-label="Recipient's username"
                  aria-describedby="basic-addon2"
                />
                <span class="input-group-text" id="basic-addon2"
                  ><i class="fa-solid fa-magnifying-glass"></i
                ></span>
              </div>
            </div>
            <div>
              <span class="d-inline"><i class="fa-regular fa-user"></i></span>

              <!-- Cart Drawer Modal -->
              <div class="d-inline cart-sidebar">
                <div class="d-inline">
                  <a class="text-decoration-none" @click="toggleCart">
                    <i class="fa-solid fa-cart-shopping"></i>
                  </a>
                </div>
                <!--  -->
                <NavCart :showCart="showCart" @close="closeCart" />
                <div
                  class="overlay"
                  :class="{ show: showCart }"
                  @click="handleClickOutside"
                ></div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </nav>
  </header>
</template>

<style lang="scss" scoped>
$primary-color: #577537;

.header-top {
  .header-social span {
    padding: 0px 5px;
    color: $primary-color;
    &:last-child {
      padding-right: 0px;
    }
  }
  .fa-clock {
    color: $primary-color;
  }
}

header {
  .navbar-brand img {
    width: 120px;
  }

  .nav-link {
    color: $primary-color;
    font-weight: 500;
    font-size: 17px;
  }

  .nav-item {
    padding: 0px 5px;
  }

  .dropdown-toggle::after {
    display: none;
  }

  .dropdown {
    padding: 0px 4px;
  }


  .fa-user {
    font-size: 20px;
    padding-left: 10px;
    color: $primary-color;
  }

  // cart
  .fa-cart-shopping {
    text-align: center;
    position: relative;
    color: $primary-color;
    font-size: 20px;
    padding: 0;
    padding-left: 10px;
  }

  .dropdown-toggle {
    color: $primary-color;
  }

  .input-group {
    border: 0px;
    background-color: #e9ecef;
    border-radius: 50px;

    .form-control {
      border: 0px;
      border-radius: 0px;
      background-color: transparent;

      &:focus {
        box-shadow: none;
      }
    }

    .input-group-text {
      border: 0px;
      border-radius: 0px;
      background-color: transparent;
    }
  }

  .rating {
    .fa-star {
      font-size: 12px;
      color: $primary-color;
    }

    p {
      color: $primary-color;
      font-weight: 700;
    }
  }

  @keyframes fadeIn {
    from {
      opacity: 0;
    }

    to {
      opacity: 1;
    }
  }

  // Assigning the above animation to all dropdown menus
  .dropdown-menu {
    &.show {
      -webkit-animation: fadeIn 0.3s alternate;
      animation: fadeIn 0.3s alternate;
    }
    padding: 6px;
    border: 0;
  }


  // Mega Menu adjustments
  .nav-item.dropdown.dropdown-mega {
    position: static;

    .dropdown-menu {
      width: 90%;
      top: auto;
      left: 5%;
    }
  }

  // Complete styles for main navbar toggler and hamburger menu
  .navbar-toggler {
    border: none;
    padding: 0;
    outline: none;

    &:focus {
      box-shadow: none;
    }
  }
  h5 {
    color: $primary-color;
  }
  .dropdown-item {
    font-weight: 500;
  }
  .dropdown-item:hover {
    background-color: #e9ecef;
    color: $primary-color;
    border-radius: 7px;
  }
}

.header-big-sale-img {
  background: rgba(0, 0, 0, 0) url(img/tastydaily-0455830109.jpg) repeat scroll
    0 0 / cover;
  background-position: bottom right;
  background-size: cover;
  border-radius: 20px;
  padding: 35px 30px 60px 30px;
}

.dropdown:hover .dropdown-menu {
  display: block;
}
</style>
