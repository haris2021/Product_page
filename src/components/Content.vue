<template>
  <div>
    <div class="row">
      <div id="left" class="col-lg-2 col-md-12 " style="margin-top:70px;">
        <h3 style="text-align:center; font-family: 'Lexend Deca'">Filters</h3>
        <div id="categ">
          <h6>Categories :</h6>
        </div>
        <div id="check">
          <label class="container" style="font-family: 'Poppins"
            >Men
            <input type="checkbox" checked="checked" />
            <span class="checkmark"></span>
          </label>
          <label class="container" style="font-family: 'Poppins"
            >Woman
            <input type="checkbox" />
            <span class="checkmark"></span>
          </label>
          <label class="container" style="font-family: 'Poppins"
            >Kids
            <input type="checkbox" />
            <span class="checkmark"></span>
          </label>
        </div>
        <hr id="horizontal" />
        <div id="size">
          <h6>Size:</h6>
        </div>
        <div id="circles">
          <div style="margin-right:7px; cursor: pointer;" class="res-circle1">
            <div class="circle-text">S</div>
          </div>
          <div style="margin-right:7px; cursor: pointer;" class="res-circle1">
            <div class="circle-text">M</div>
          </div>
          <div style="margin-right:7px; cursor: pointer;" class="res-circle1">
            <div class="circle-text">L</div>
          </div>
          <div style="margin-right:7px; cursor: pointer;" class="res-circle1">
            <div class="circle-text">XL</div>
          </div>

          <div style="margin-right:7px; cursor: pointer;" class="res-circle1">
            <div class="circle-text">XXL</div>
          </div>
        </div>

        <hr id="h2" />

        <div id="range">
          <h5>Price Range</h5>
        </div>

        <div id="min-max">
          <div id="min">
            <h5 style="margin-left:20px">Min</h5>

            <div>
              <input
                type="number"
                id="quantity"
                name="quantity"
                step="100"
                min="1"
                max="500"
              />
            </div>
          </div>

          <i id="arrow" class="fas fa-long-arrow-alt-right"></i>

          <div id="max">
            <h5 style="margin-left:15px">Max</h5>

            <div>
              <input
                type="number"
                id="quantity"
                name="quantity"
                step="100"
                min="1"
                max="500"
              />
            </div>
          </div>
        </div>

        <div id="range-btn">
          <button
            id="range-btn1"
            type="submit"
            style="background-color: #40ff00; border-radius:10px;"
          >
            Set price
          </button>
        </div>

        <hr id="h3" />

        <div id="colours">
          <h5>Colors</h5>
        </div>

        <div id="listcolors1">
          <div
            style="margin-right:7px ;   background:  #40ff00;"
            class="s-circle"
          ></div>
          <div
            style="margin-right:7px; background: #cc0044;  cursor: pointer; "
            class="s-circle"
          ></div>
          <div
            style="margin-right:7px ; background:#ffff33;   cursor: pointer;"
            class="s-circle"
          ></div>
          <div
            style="margin-right:7px ; background:  #3d3d29;  cursor: pointer; "
            class="s-circle"
          ></div>

          <div
            style="margin-right:7px; background:#4d4dff;  cursor: pointer;"
            class="s-circle"
          ></div>
        </div>

        <div id="listcolors2">
          <div
            style="margin-right:7px ;   background:  #ff33ff;  cursor: pointer;"
            class="s-circle"
          ></div>
          <div
            style="margin-right:7px; background: #ffa64d ;   cursor: pointer; "
            class="s-circle"
          ></div>
          <div
            style="margin-right:7px ; background: #8533ff;  cursor: pointer; "
            class="s-circle"
          ></div>
          <div
            style="margin-right:7px ; background: #ff8533;   cursor: pointer;"
            class="s-circle"
          ></div>

          <div
            style="margin-right:7px; background: #f2f2f2;  cursor: pointer;"
            class="s-circle"
          ></div>
        </div>
      </div>

      <div id="right" class="col-lg-10 col-md-12" style="border-left:1px solid black; margin-top:70px">
        <div id="top">
          <h5>Search results for "Shirt for men"</h5>
        </div>

        <div id="sort">
          <h5 stye="font-weight:bold">Sort:</h5>

          <div id="sort-btn">
            <button id="btn-mobile"
              style="border-radius:10px ; margin-right:30px ;  width:140px; font-family: 'Poppins' ; "
            >
              Relevance
            </button>
            <button id="btn-mobile"
              style="border-radius:10px ; margin-right:30px ; width:140px ; font-family: 'Poppins'"
            >
              Popular
            </button>
            <button id="btn-mobile"
              style="border-radius:10px ; margin-right:30px ; width:140px ;font-family: 'Poppins'"
            >
              Most New
            </button>
            <button id="btn-mobile"
              style="border-radius:10px ; margin-right:30px; width:140px; font-family: 'Poppins'"
            >
              Price
            </button>
          </div>
        </div>
        <br />
        <div
          class="row"
          style="justify-content: space-evenly ; margin-left:0 ; margin-right:0px;"
        >
          <div
            class="card col-6 col-md-2 "
            v-for="card in cards"
            :key="card.cardId"
            id="card-whole"
          >
          <div class="container1">
            <img class="card-img" v-bind:src="card.cardImage" alt="" />
            <div class="postioner">

                 <div id="heart-icon"><i class="fas fa-heart"></i></div>
            </div>

          </div>
            <div class="card-info">
              <h4 class="card-title">{{ card.cardTitle }}</h4>
              <h6 class="circles-card">
                
                <div
                  style="margin-right:7px; background:red;  cursor: pointer;"
                  class="c-circle"
                ></div>
                <div
                  style="margin-right:7px; background:#4d4dff;  cursor: pointer;"
                  class="c-circle"
                ></div>
                <div
                  style="margin-right:7px; background:yellow;  cursor: pointer;"
                  class="c-circle"
                ></div>
                <div
                  style="margin-right:7px; background:black;  cursor: pointer;"
                  class="c-circle"
                ></div>
              </h6>
              <h4 class="card-description">{{ card.cardPrice }}</h4>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- <div class="content" style="float:left">
    <div class="row" >
      <div class="col-2">
        <h3 style="text-align:center">Filters</h3>
        <div id="categ">
          <h6>Categories :</h6>
        </div>
        <div id="check">
          <label class="container"
            >Men
            <input type="checkbox" checked="checked" />
            <span class="checkmark"></span>
          </label>
          <label class="container"
            >Woman
            <input type="checkbox" />
            <span class="checkmark"></span>
          </label>
          <label class="container"
            >Kids
            <input type="checkbox" />
            <span class="checkmark"></span>
          </label>
        </div>
        <hr id="horizontal" />
        <div id="size">
          <h6>Size:</h6>
        </div>
        <div id="circles">
          <div style="margin-right:7px" class="res-circle1">
            <div class="circle-text">S</div>
          </div>
          <div style="margin-right:7px" class="res-circle1">
            <div class="circle-text">M</div>
          </div>
          <div style="margin-right:7px" class="res-circle1">
            <div class="circle-text">L</div>
          </div>
          <div style="margin-right:7px" class="res-circle1">
            <div class="circle-text">XL</div>
          </div>

          <div style="margin-right:7px" class="res-circle1">
            <div class="circle-text">XXL</div>
          </div>
        </div>

        <hr id="h2" />

        <div id="range">
          <h5>Price Range</h5>
        </div>

        <div id="min-max">
          <div id="min">
            <h5 style="text-align:center">Min</h5>

            <div>
              <input
                type="number"
                id="quantity"
                name="quantity"
                step="100"
                min="1"
                max="500"
              />
            </div>
          </div>

          <i id="arrow" class="fas fa-long-arrow-alt-right"></i>

          <div id="max">
            <h5 style="text-align:center">Max</h5>

            <div>
              <input
                type="number"
                id="quantity"
                name="quantity"
                step="100"
                min="1"
                max="500"
              />
            </div>
          </div>
        </div>

        <div id="range-btn">
          <button type="submit" style="background-color: #40ff00; border-radius:10px;">Set price</button>
        </div>

        <hr id="h3" />

        <div id="colours">
          <h5>Colors</h5>
        </div>

        <div id="listcolors1">
          <div
            style="margin-right:7px ;   background:  #40ff00;"
            class="s-circle"
          ></div>
          <div
            style="margin-right:7px; background: #cc0044; "
            class="s-circle"
          ></div>
          <div
            style="margin-right:7px ; background:#ffff33; "
            class="s-circle"
          ></div>
          <div
            style="margin-right:7px ; background:  #3d3d29; "
            class="s-circle"
          ></div>

          <div
            style="margin-right:7px; background:#4d4dff;"
            class="s-circle"
          ></div>
        </div>

        <div id="listcolors2">
          <div
            style="margin-right:7px ;   background:  #ff33ff;"
            class="s-circle"
          ></div>
          <div
            style="margin-right:7px; background: #ffa64d ; "
            class="s-circle"
          ></div>
          <div
            style="margin-right:7px ; background: #8533ff; "
            class="s-circle"
          ></div>
          <div
            style="margin-right:7px ; background: #ff8533; "
            class="s-circle"
          ></div>

          <div
            style="margin-right:7px; background: #f2f2f2;"
            class="s-circle"
          ></div>
        </div>
      </div>

      <div class="col-7" style="border-left:5px solid black; margin-left:10px;">
        <div id="top">
          <h5>Search results for "Shirt for men"</h5>
        </div>

        <div id="sort">
          <h5 stye="font-weight:bold">Sort:</h5>

          <div id="sort-btn">
            <button style="border-radius:10px ; margin-right:10px">
              Relevance
            </button>
            <button style="border-radius:10px ; margin-right:10px">
              Relevance
            </button>
            <button style="border-radius:10px ; margin-right:10px">
              Relevance
            </button>
            <button style="border-radius:10px ; margin-right:10px">
              Relevance
            </button>
          </div>
        </div>
      </div>

      <div class="container-flex ">
          <div class="row gx-0 padding" style="justify-content: space-around">
            <div class="card col-2" v-for="card in cards" :key="card.cardId">
              <img class="card-img" v-bind:src="card.cardImage" alt="" />
              <div class="card-info">
                <h4 class="card-title" >{{ card.cardTitle }}</h4>
                <h4 class="card-description">&#8377; {{ card.cardPrice }}</h4>
              </div>
            </div>
          </div>
        </div>
    </div>
   </div> -->
</template>

<script>
export default {
  data() {
    return {
      cards: [
        {
          cardId: "1",
          cardImage:
            "https://images.unsplash.com/photo-1576566588028-4147f3842f27?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80",
          cardTitle: "Blue Formal Tshirt men",
          cardPrice: "1000",
        },
        {
          cardId: "2",
          cardImage:
            "https://images.unsplash.com/photo-1576566588028-4147f3842f27?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80",
          cardTitle: "Blue Formal Tshirt men",
          cardPrice: "1000",
        },
        {
          cardId: "3",
          cardImage:
            "https://images.unsplash.com/photo-1576566588028-4147f3842f27?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80",
          cardTitle: "Blue Formal Tshirt men",
          cardPrice: "1000",
        },
        {
          cardId: "4",
          cardImage:
            "https://images.unsplash.com/photo-1576566588028-4147f3842f27?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80",
          cardTitle: "Blue Formal Tshirt men",
          cardPrice: "1000",
        },
        {
          cardId: "5",
          cardImage:
            "https://images.unsplash.com/photo-1576566588028-4147f3842f27?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80",
          cardTitle: "Blue Formal Tshirt men",
          cardPrice: "1000",
        },
        {
          cardId: "6",
          cardImage:
            "https://images.unsplash.com/photo-1576566588028-4147f3842f27?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80",
          cardTitle: "Blue Formal Tshirt men",
          cardPrice: "1000",
        },
        {
          cardId: "7",
          cardImage:
            "https://images.unsplash.com/photo-1576566588028-4147f3842f27?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80",
          cardTitle: "Blue Formal Tshirt men",
          cardPrice: "1000",
        },
        {
          cardId: "8",
          cardImage:
            "https://images.unsplash.com/photo-1576566588028-4147f3842f27?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80",
          cardTitle: "Blue Formal Tshirt men",
          cardPrice: "1000",
        },
        {
          cardId: "9",
          cardImage:
            "https://images.unsplash.com/photo-1576566588028-4147f3842f27?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80",
          cardTitle: "Blue Formal Tshirt men",
          cardPrice: "1000",
        },
        {
          cardId: "10",
          cardImage:
            "https://images.unsplash.com/photo-1576566588028-4147f3842f27?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80",
          cardTitle: "Blue Formal Tshirt men",
          cardPrice: "1000",
        },
      ],
    };
  },
};
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
* {
  box-sizing: border-box;
}

/* Create two unequal columns that floats next to each other */
.column {
  float: left;
  padding: 10px;
  height: 800px; /* Should be removed. Only for demonstration */
}

.left {
  width: 25%;
}

.right {
  width: 75%;
}

/* Clear floats after the columns */
/* .row:after {
  content: "";
  display: table;
  clear: both;
} */

.content {
  margin-top: 60px;
}

.container {
  display: block;
  position: relative;
  padding-left: 35px;
  margin-bottom: 12px;
  cursor: pointer;
  font-size: 15px;
  font-family: "Times New Roman", Times, serif;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

/* Hide the browser's default checkbox */
.container input {
  position: absolute;
  opacity: 0;
  cursor: pointer;
  height: 10px;
  width: 10px;
}

/* Create a custom checkbox */
.checkmark {
  position: absolute;
  top: 0;
  left: 0;
  height: 17px;
  width: 17px;
  background-color: #eee;
}

/* On mouse-over, add a grey background color */
.container:hover input ~ .checkmark {
  background-color: rgb(155, 139, 139);
}

/* When the checkbox is checked, add a blue background */
.container input:checked ~ .checkmark {
  background-color: #40ff00;
}

/* Create the checkmark/indicator (hidden when not checked) */
.checkmark:after {
  content: "";
  position: absolute;
  display: none;
}

/* Show the checkmark when checked */
.container input:checked ~ .checkmark:after {
  display: block;
}

/* Style the checkmark/indicator */
.container .checkmark:after {
  left: 3px;
  top: 3px;
  width: 4px;
  height: 5px;
  border: solid white;
  border-width: 0 3px 3px 0;
  -webkit-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  transform: rotate(45deg);
}

#check {
  margin-left: 60px;
  margin-top: 13px;
  font-family: "Poppins";
}

#categ {
  margin-left: 25px;
}

#horizontal {
  border-top: 1px solid black;
  width: 90%;
}

#h2 {
  border-top: 1px solid black;
  width: 90%;
  margin-top: 80px;
}
.res-circle1 {
  background: #dfe1e7;
  clip-path: circle(50%);
  height: 2em;
  width: 2em;
}

.circle-text {
  text-align: center;
  padding-top: 4px;
  font-family: Arial, Helvetica, sans-serif;
}

#circles {
  float: left;
  display: flex;
  margin-left: 25px;
  margin-top: 10px;
}

#listcolors1 {
  float: left;
  display: flex;
  margin-left: 30px;
  margin-top: 10px;
}

#listcolors2 {
  float: left;
  display: flex;
  margin-top: 20px;
  margin-left: 30px;
}
#size {
  margin-left: 65px;
  font-family: "Poppins";
}

#h3 {
  border-top: 1px solid black;
  width: 90%;
  margin-top: 30px;
}

.s-circle {
  height: 2em;
  width: 2em;
  clip-path: circle(50%);
}

#colours {
  text-align: center;
  font-family: "Lexend Deca";
}

#range {
  text-align: center;
  font-family: "Lexend Deca";
}

#range-btn {
  text-align: center;
  margin-top: 25px;
}

#range-btn1 {
  width: 100px;
  height: 45px;
  font-family: "Lexend Deca";
  font-size: 11px;
  text-transform: uppercase;
  letter-spacing: 2.5px;
  font-weight: 500;
  color: #000;
  background-color: #fff;
  border: none;
  border-radius: 45px;
  box-shadow: 0px 8px 15px rgba(0, 0, 0, 0.1);
  transition: all 0.3s ease 0s;
  cursor: pointer;
  outline: none;
}

.content {
  margin-left: 100px;
}

#top {
  margin-left: 20px;
}

#sort {
  margin-left: 20px;
  margin-top: 20px;
  display: flex;
}

#sort-btn {
  margin-left: 10px;
}

#arrow {
  position: relative;
  top: 40px;
  font-size: 20px;
}

#min-max {
  display: flex;
  justify-content: space-between;
}

.card-img {
  border-radius: 20px;
  height: 250px;
  width: 100%;
  margin-top: 20px;
  box-shadow: rgba(0, 0, 0, 0.07) 0px 1px 2px, rgba(0, 0, 0, 0.07) 0px 2px 4px,
    rgba(0, 0, 0, 0.07) 0px 4px 8px, rgba(0, 0, 0, 0.07) 0px 8px 16px,
    rgba(0, 0, 0, 0.07) 0px 16px 32px, rgba(0, 0, 0, 0.07) 0px 32px 64px;
}

.card {
  border: none;
  height: 400px;
  min-width: 250px;
  margin-bottom: 15px;
}
/* #cloths
{
   height: 50%;
   margin-top:150px;  
   position: absolute;
   right:400px;
  
} */

.card-info {
  width: 100%;
  border-radius: 20px;
  margin-top: 20px;
  padding-left: 50px;
}
.card-title {
  font-size: 10px;
  padding-top: 10px;
}

.card-description {
  color: #40ff00;
  padding-left:20px;
  padding-top:20px;
}

.circles-card {
  color: #40ff00;
  font-size: 10px;
  background-color: white;
  margin-right: 40px;
  margin-bottom: 10px;
  padding-left: 20px;
}

.c-circle {
  height: 1em;
  width: 1em;
  clip-path: circle(50%);
  display: flex;
  float: left;

}

.postioner
{
  width: 100%;
  height:10%;
  position: absolute;
  left: 0;
  top: 0;
  margin-top:30px;
  padding-left:200px;
  border-radius: 20px;

}

#heart-icon
{
  position: relative;
  bottom:20px;
  cursor: pointer;
  border-radius: 20px;
  background-color: #40ff00;
  margin-top:20px;
  padding-left: 6px;
  padding-top: 5px;
  width: 32px;
  height: 32px;

}

@media  screen and (max-width: 768px) {
   
    #left
    {
        width:100%;
       padding:20px;

    }

    #right
    {
      width: 100%;
    }

    #categ
    {
         padding-left: 180px;
    }
     
     #check
    {
            padding-left: 190px;
    }

    #size
   {
        margin-left:20px;
        padding-left:180px;
   }

      #circles
    {
        padding-left: 190px;
    }


    #min
    {
          margin-left: 210px;
    }

    #max
    {
      margin-right: 180px;
    }

    #listcolors1
    {
      margin-left: 100px;
      padding-left:24px;
    }

    #listcolors2
    {
      margin-left:120px;
            padding-left:24px;
            margin-bottom: 20px;
            margin-top:15px;
    }

    #top
    {
       width:400px;
       margin-left:220px;
       margin-top: -50px;

    }

    #btn-mobile
    {
       margin-left:40px;
       margin-bottom: 10px;
    }
}

@media screen and (max-width: 320px){
   
    #left
    {
        width:100%;
       padding:20px;

    }

    #right
    {
      width: 100%;
    }

     #categ
    {
         padding-left: 30px;
    }
    #circles
    {
        padding-left: 40px;
    }

    #check
    {
            padding-left: 20px;
            margin-left: 100px;
    }

   #size
   {
        margin-left:20px;
        padding-left:10px;
   }

    #min
    {
          margin-left: 40px;
    }

    #max
    {
      margin-right: 40px;
    }

    #listcolors1
    {
      margin-right: 30px;
      padding-left:-1px;
      margin-left: 54px;
    }

    #listcolors2
    {
      margin-right: 30px;
            padding-left:24px;
                  margin-left: 54px;

    }

    #top
    {
       width:400px;
       margin-left:50px;

    }

    #btn-mobile
    {
       margin-left:50px;
       margin-bottom: 15px;
    }

    #horizontal {
 border-top: 1px solid black;
  width: 90%;
  margin-left: 40px;
}

#h2 {
  border-top: 1px solid black;
  width: 90%;
  margin-top: 80px;
  margin-left: 40px;
}

#card-whole
{
    margin-left:67px;
}
}


</style>
