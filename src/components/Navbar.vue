<script setup>
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
            ><i class="fa-solid fa-headphones-simple"></i> +1 900 777525</span
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
      <div class="container-fluid">
        <a class="navbar-brand" href="#"><img :src="logo" alt="" /></a>
        <button
          class="navbar-toggler collapsed"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbar-content"
        >
          <div class="hamburger-toggle">
            <div class="hamburger">
              <span></span>
              <span></span>
              <span></span>
            </div>
          </div>
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
                ><i class="fa-solid fa-shop"></i> Shop</a
              >
              <div class="dropdown-menu shadow">
                <div class="mega-content px-4">
                  <div class="container-fluid">
                    <div class="row">
                      <div class="col-12 col-sm-4 col-md-3 py-4">
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
                      <div class="col-12 col-sm-4 col-md-3 py-4">
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
                      <div class="col-12 col-sm-4 col-md-3 py-4">
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
                      <div class="col-12 col-sm-4 col-md-3 py-4">
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
                ><i class="fa-solid fa-pepper-hot"></i> Vegetables</a
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
                ><i class="fa-solid fa-apple-whole"></i> Fresh Fruits</a
              >
              <div class="dropdown-menu shadow">
                <div class="mega-content px-4">
                  <div class="container-fluid">
                    <div class="row">
                      <div class="col-12 col-sm-3 col-md-3 py-4">
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
                      <div class="col-12 col-sm-3 col-md-3 py-4">
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
                      <div class="col-12 col-sm-3 col-md-3 py-4">
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
                      <div class="col-12 col-sm-3 col-md-3 py-4">
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
                ><i class="fa-solid fa-drumstick-bite"></i> Meat</a
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
                ><i class="fa-solid fa-fish"></i> Seafood</a
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
                ><i class="fa-solid fa-bread-slice"></i> Baking</a
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
                ><i class="fa-solid fa-champagne-glasses"></i> Drinks</a
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
                ><i class="fa-solid fa-list"></i> Others</a
              >
              <ul class="dropdown-menu shadow">
                <li>
                  <a class="dropdown-item" href="#">Household Cleaners</a>
                </li>
                <li>
                  <a class="dropdown-item" href="blog.html"
                    >Personal Care Products (e.g., shampoo, toothpaste)</a
                  >
                </li>
                <li>
                  <a class="dropdown-item" href="#">
                    Canned Goods (e.g., soups, vegetables)</a
                  >
                </li>
                <li>
                  <a class="dropdown-item" href="#"> Breakfast Cereals</a>
                </li>
                <li>
                  <a class="dropdown-item" href="#">
                    Snack Items (e.g., chips, nuts)</a
                  >
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
              <span class="d-inline"><i class="fa-solid fa-user"></i></span>

              <!-- Cart Drawer Modal -->
              <div class="content d-inline">
                <a class="text-decoration-none menu-click">
                  <i
                    data-count="3"
                    class="fa-solid fa-cart-shopping badge d-inline"
                  ></i>
                </a>
              </div>
              <!--  -->
              <div class="menu px-2">
                <a class="btn menu-click">
                  <i class="fa fa-times" aria-hidden="true"></i>
                </a>
                <h5 class="py-3">Shopping Cart 2</h5>
                <table class="table text-white table-borderless">
                  <thead>
                    <tr>
                      <th scope="col">Item</th>
                      <th scope="col">Price</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td>Potato</td>
                      <td>10</td>
                    </tr>
                    <tr>
                      <td>Chicken</td>
                      <td>200</td>
                    </tr>
                  </tbody>
                  <thead class="border-0">
                    <tr class="border-0">
                      <th scope="col">Subtotal</th>
                      <th scope="col">300</th>
                    </tr>
                  </thead>
                </table>
                <button class="btn btn-outline-primary w-100 mt-2">
                  View Cart <i class="fa-solid fa-cart-shopping"></i>
                </button>
                <button class="btn btn-outline-warning w-100 mt-2">
                  Checkout <i class="fa-solid fa-check"></i>
                </button>
              </div>
              <div class="overlay"></div>
            </div>
          </div>
        </div>
      </div>
    </nav>
  </header>
</template>

<style lang="scss">
$primary-color: #577537;

.header-top {
  .header-social span {
    padding: 0px 5px;
    color: $primary-color;
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
    padding-right: 20px;
  }

  //  .badge:after {
  //   content: attr(data-count);
  //   position: absolute;
  //   background: #f60;
  //   text-align: center;
  //   line-height: 2rem;
  //   font-size: 1rem;
  //   border-radius: 50%;
  //   color: #fff;
  //   border: 1px solid #f60;
  //   font-family: sans-serif;
  //   font-weight: bold;
  //   right: 0px;
  //   top: -20px;
  //   height: 25px;
  //   width: 25px;
  //   display: flex;
  //   align-items: center;
  //   justify-content: center;
  // }

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

    .hamburger-toggle {
      position: relative;
      display: inline-block;
      width: 50px;
      height: 50px;
      z-index: 11;
      // float: right;

      .hamburger {
        position: absolute;
        transform: translate(-50%, -50%) rotate(0deg);
        left: 50%;
        top: 50%;
        width: 50%;
        height: 50%;
        pointer-events: none;

        span {
          width: 100%;
          height: 4px;
          position: absolute;
          background: #333;
          border-radius: 2px;
          z-index: 1;
          transition: transform 0.2s cubic-bezier(0.77, 0.2, 0.05, 1),
            background 0.2s cubic-bezier(0.77, 0.2, 0.05, 1),
            all 0.2s ease-in-out;
          left: 0px;

          &:first-child {
            top: 10%;
            transform-origin: 50% 50%;
            transform: translate(0% -50%) !important;
          }

          &:nth-child(2) {
            top: 50%;
            transform: translate(0, -50%);
          }

          &:last-child {
            left: 0px;
            top: auto;
            bottom: 10%;
            transform-origin: 50% 50%;
          }
        }

        &.active {
          span {
            position: absolute;
            margin: 0;

            &:first-child {
              top: 45%;
              transform: rotate(45deg);
            }

            &:nth-child(2) {
              left: 50%;
              width: 0px;
            }

            &:last-child {
              top: 45%;
              transform: rotate(-45deg);
            }
          }
        }
      }
    }
  }
  h5 {
    color: $primary-color;
  }
  // drawer
  .menu {
    h5 {
      color: #fff;
    }
    .btn {
      color: white;
      .fa {
        margin-left: 8px;
      }
    }
    background-color: $primary-color;
    top: 0;
    width: 250px;
    height: 100vh;
    position: fixed;
    right: -250px;
    transition: all 0.2s ease-out;
    z-index: 9999;
  }
}

.header-big-sale-img {
    background: rgba(0, 0, 0, 0) url(img/tastydaily-0455830109.jpg) repeat scroll 0 0 / cover;
    background-position: bottom right;
    background-size: cover;
    border-radius: 20px;
    padding: 35px 30px 60px 30px;
}
</style>
