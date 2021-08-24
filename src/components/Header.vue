<template>
 
 <div class="container-fluid navbar-container">
    <div class="row mb-2 d-flex" style="justify-content: space-around">
      <div class="logo navbar-brand">
        <a href="#"><img src="logo.jpg" alt="Logo" width="260px"/></a>
      </div>
      <div class="input-container">
        <form class="d-flex">
          <input
            class="form-control"
            type="search"
            placeholder="Search products here.."
            aria-label="Search"
          />
          <button class="btn" type="submit">
            <i class="fas fa-search"></i>
          </button>
        </form>
      </div>
      <div class="user-details d-flex">
        <div class="d-flex u">
          <p style="font-family: 'Poppins';
">My Account</p>
          <i class="fas fa-angle-down"></i>
        </div>
        <div class="d-flex u">
          <i class="fas fa-shopping-cart"></i>
          <p style="font-family: 'Poppins'">My Cart</p>
        </div>
      </div>
    </div>

    <div class="header">
        <b-navbar  >
          <b-navbar-nav variant="light" >
        <nav class="navbar navbar-expand-lg navbar-light"
        style="justify-content: center" >
            <!-- Navbar dropdowns -->
            <b-nav-item-dropdown  style="font-family: 'Lexend Deca';  font-weight:bolder ; padding-right:15px;
" text="ACCESSORIES" right>
              <b-dropdown-item href="#">EN</b-dropdown-item>
              <b-dropdown-item href="#">ES</b-dropdown-item>
              <b-dropdown-item href="#">RU</b-dropdown-item>
              <b-dropdown-item href="#">FA</b-dropdown-item>
            </b-nav-item-dropdown>

            <b-nav-item-dropdown text="MEN" style="font-family: 'Lexend Deca'; font-weight:bolder ;padding-right:15px; " right>
              <b-dropdown-item href="#">Account</b-dropdown-item>
              <b-dropdown-item href="#">Settings</b-dropdown-item>
            </b-nav-item-dropdown>

            <b-nav-item-dropdown style="font-family: 'Lexend Deca'; font-weight:bolder;padding-right:15px;r" text="WOMAN">
              <b-dropdown-item href="#">Account</b-dropdown-item>
              <b-dropdown-item href="#">Settings</b-dropdown-item>
            </b-nav-item-dropdown>
            <b-nav-item-dropdown style="font-family: 'Lexend Deca'; font-weight:bolder;padding-right:15px;" text="Kids">
              <b-dropdown-item href="#">Account</b-dropdown-item>
              <b-dropdown-item href="#">Settings</b-dropdown-item>
            </b-nav-item-dropdown>
            <b-nav-item-dropdown style="font-family: 'Lexend Deca'; font-weight:bolder;padding-right:15px;" text="Electrocnics">
              <b-dropdown-item href="#">Account</b-dropdown-item>
              <b-dropdown-item href="#">Settings</b-dropdown-item>
            </b-nav-item-dropdown>

            <b-nav-item-dropdown text="Shoes & More" style="font-family: 'Poppins', sans-serif; font-weight:bolder">
              <b-dropdown-item href="#">Account</b-dropdown-item>
              <b-dropdown-item href="#">Settings</b-dropdown-item>
            </b-nav-item-dropdown>
        </nav>
          </b-navbar-nav>
        </b-navbar>
    </div>
  </div>


  
</template>

//
<script>
// export default {
//   name: 'HelloWorld',
//   props: {
//     msg: String
//   }
// }
//
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
* {
  border: 0;
  padding: 0;
  margin: 0;
}

.navbar-container {
  height: 100px;
  background: white;
  box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
  padding-top: 40px;
}

.logo {
  width: 22%;
  height: 50px;
}

.input-container {
  width: 40%;
  border: none;
  position: relative;
}

input[type] {
  height: 40px;
  background: #e5e5e5;
  color: #737373;
  font-size: 22px;
  text-indent: 5px;
  box-shadow: rgba(0, 0, 0, 0.24) 0px 1px 5px;
}

.btn {
  border: none;
  background: #70e000;
  position: absolute;
  right: 15px;
}

.user-details {
  width: 25%;
  height: 40px;
  justify-content: space-evenly;
}

.user-details i {
  margin-top: 5px;
  margin-left: 8px;
  margin-right: 8px;
  font-size: 20px;
}

.navbar-expand-lg .navbar-nav .nav-link {
  padding-right: 2rem;
  padding-left: 2rem;
  letter-spacing: 5px;
  padding-top: 0.75rem;
}

li a {
  font-size: 20px;
  font-weight: bolder;
  color: black;
}

.header
{
      justify-content: center;
}

.navbar-expand {
    flex-flow: row nowrap;
    justify-content: center;
}

b-nav-item-dropdown
{
    padding-right: 10px;
}

</style>
