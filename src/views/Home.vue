<template>
  <div class="home">
<div class="jumbotron jumbotron-fluid" v-if="!loading">
  <div class="container">
    <h1 class="display-4">CHECK THE WEATHER</h1>
    <p class="lead">FIND YOUR CITY</p>
  </div>
</div>
    <v-container>
      <v-layout>
        <v-flex md4 sm4 offset-md4 offset-sm4>
          <v-text-field
            v-model="city"
            :counter="20"
            label="City"
            required
          ></v-text-field>
          <div style="margin: 20px 0 20px 0">
          <select class="custom-select" placeholder="Select the country" v-model="countryCode">
          <option value="" disabled selected>Select the country</option>
            <option value="AF">Afghanistan</option>
            <option value="AX">Åland Islands</option>
            <option value="AL">Albania</option>
            <option value="DZ">Algeria</option>
            <option value="AS">American Samoa</option>
            <option value="AD">Andorra</option>
            <option value="AO">Angola</option>
            <option value="AI">Anguilla</option>
            <option value="AQ">Antarctica</option>
            <option value="AG">Antigua and Barbuda</option>
            <option value="AR">Argentina</option>
            <option value="AM">Armenia</option>
            <option value="AW">Aruba</option>
            <option value="AU">Australia</option>
            <option value="AT">Austria</option>
            <option value="AZ">Azerbaijan</option>
            <option value="BS">Bahamas</option>
            <option value="BH">Bahrain</option>
            <option value="BD">Bangladesh</option>
            <option value="BB">Barbados</option>
            <option value="BY">Belarus</option>
            <option value="BE">Belgium</option>
            <option value="BZ">Belize</option>
            <option value="BJ">Benin</option>
            <option value="BM">Bermuda</option>
            <option value="BT">Bhutan</option>
            <option value="BO">Bolivia, Plurinational State of</option>
            <option value="BQ">Bonaire, Sint Eustatius and Saba</option>
            <option value="BA">Bosnia and Herzegovina</option>
            <option value="BW">Botswana</option>
            <option value="BV">Bouvet Island</option>
            <option value="BR">Brazil</option>
            <option value="IO">British Indian Ocean Territory</option>
            <option value="BN">Brunei Darussalam</option>
            <option value="BG">Bulgaria</option>
            <option value="BF">Burkina Faso</option>
            <option value="BI">Burundi</option>
            <option value="KH">Cambodia</option>
            <option value="CM">Cameroon</option>
            <option value="CA">Canada</option>
            <option value="CV">Cape Verde</option>
            <option value="KY">Cayman Islands</option>
            <option value="CF">Central African Republic</option>
            <option value="TD">Chad</option>
            <option value="CL">Chile</option>
            <option value="CN">China</option>
            <option value="CX">Christmas Island</option>
            <option value="CC">Cocos (Keeling) Islands</option>
            <option value="CO">Colombia</option>
            <option value="KM">Comoros</option>
            <option value="CG">Congo</option>
            <option value="CD">Congo, the Democratic Republic of the</option>
            <option value="CK">Cook Islands</option>
            <option value="CR">Costa Rica</option>
            <option value="CI">Côte d'Ivoire</option>
            <option value="HR">Croatia</option>
            <option value="CU">Cuba</option>
            <option value="CW">Curaçao</option>
            <option value="CY">Cyprus</option>
            <option value="CZ">Czech Republic</option>
            <option value="DK">Denmark</option>
            <option value="DJ">Djibouti</option>
            <option value="DM">Dominica</option>
            <option value="DO">Dominican Republic</option>
            <option value="EC">Ecuador</option>
            <option value="EG">Egypt</option>
            <option value="SV">El Salvador</option>
            <option value="GQ">Equatorial Guinea</option>
            <option value="ER">Eritrea</option>
            <option value="EE">Estonia</option>
            <option value="ET">Ethiopia</option>
            <option value="FK">Falkland Islands (Malvinas)</option>
            <option value="FO">Faroe Islands</option>
            <option value="FJ">Fiji</option>
            <option value="FI">Finland</option>
            <option value="FR">France</option>
            <option value="GF">French Guiana</option>
            <option value="PF">French Polynesia</option>
            <option value="TF">French Southern Territories</option>
            <option value="GA">Gabon</option>
            <option value="GM">Gambia</option>
            <option value="GE">Georgia</option>
            <option value="DE">Germany</option>
            <option value="GH">Ghana</option>
            <option value="GI">Gibraltar</option>
            <option value="GR">Greece</option>
            <option value="GL">Greenland</option>
            <option value="GD">Grenada</option>
            <option value="GP">Guadeloupe</option>
            <option value="GU">Guam</option>
            <option value="GT">Guatemala</option>
            <option value="GG">Guernsey</option>
            <option value="GN">Guinea</option>
            <option value="GW">Guinea-Bissau</option>
            <option value="GY">Guyana</option>
            <option value="HT">Haiti</option>
            <option value="HM">Heard Island and McDonald Islands</option>
            <option value="VA">Holy See (Vatican City State)</option>
            <option value="HN">Honduras</option>
            <option value="HK">Hong Kong</option>
            <option value="HU">Hungary</option>
            <option value="IS">Iceland</option>
            <option value="IN">India</option>
            <option value="ID">Indonesia</option>
            <option value="IR">Iran, Islamic Republic of</option>
            <option value="IQ">Iraq</option>
            <option value="IE">Ireland</option>
            <option value="IM">Isle of Man</option>
            <option value="IL">Israel</option>
            <option value="IT">Italy</option>
            <option value="JM">Jamaica</option>
            <option value="JP">Japan</option>
            <option value="JE">Jersey</option>
            <option value="JO">Jordan</option>
            <option value="KZ">Kazakhstan</option>
            <option value="KE">Kenya</option>
            <option value="KI">Kiribati</option>
            <option value="KP">Korea, Democratic People's Republic of</option>
            <option value="KR">Korea, Republic of</option>
            <option value="KW">Kuwait</option>
            <option value="KG">Kyrgyzstan</option>
            <option value="LA">Lao People's Democratic Republic</option>
            <option value="LV">Latvia</option>
            <option value="LB">Lebanon</option>
            <option value="LS">Lesotho</option>
            <option value="LR">Liberia</option>
            <option value="LY">Libya</option>
            <option value="LI">Liechtenstein</option>
            <option value="LT">Lithuania</option>
            <option value="LU">Luxembourg</option>
            <option value="MO">Macao</option>
            <option value="MK">Macedonia, the former Yugoslav Republic of</option>
            <option value="MG">Madagascar</option>
            <option value="MW">Malawi</option>
            <option value="MY">Malaysia</option>
            <option value="MV">Maldives</option>
            <option value="ML">Mali</option>
            <option value="MT">Malta</option>
            <option value="MH">Marshall Islands</option>
            <option value="MQ">Martinique</option>
            <option value="MR">Mauritania</option>
            <option value="MU">Mauritius</option>
            <option value="YT">Mayotte</option>
            <option value="MX">Mexico</option>
            <option value="FM">Micronesia, Federated States of</option>
            <option value="MD">Moldova, Republic of</option>
            <option value="MC">Monaco</option>
            <option value="MN">Mongolia</option>
            <option value="ME">Montenegro</option>
            <option value="MS">Montserrat</option>
            <option value="MA">Morocco</option>
            <option value="MZ">Mozambique</option>
            <option value="MM">Myanmar</option>
            <option value="NA">Namibia</option>
            <option value="NR">Nauru</option>
            <option value="NP">Nepal</option>
            <option value="NL">Netherlands</option>
            <option value="NC">New Caledonia</option>
            <option value="NZ">New Zealand</option>
            <option value="NI">Nicaragua</option>
            <option value="NE">Niger</option>
            <option value="NG">Nigeria</option>
            <option value="NU">Niue</option>
            <option value="NF">Norfolk Island</option>
            <option value="MP">Northern Mariana Islands</option>
            <option value="NO">Norway</option>
            <option value="OM">Oman</option>
            <option value="PK">Pakistan</option>
            <option value="PW">Palau</option>
            <option value="PS">Palestinian Territory, Occupied</option>
            <option value="PA">Panama</option>
            <option value="PG">Papua New Guinea</option>
            <option value="PY">Paraguay</option>
            <option value="PE">Peru</option>
            <option value="PH">Philippines</option>
            <option value="PN">Pitcairn</option>
            <option value="PL">Poland</option>
            <option value="PT">Portugal</option>
            <option value="PR">Puerto Rico</option>
            <option value="QA">Qatar</option>
            <option value="RE">Réunion</option>
            <option value="RO">Romania</option>
            <option value="RU">Russian Federation</option>
            <option value="RW">Rwanda</option>
            <option value="BL">Saint Barthélemy</option>
            <option value="SH">Saint Helena, Ascension and Tristan da Cunha</option>
            <option value="KN">Saint Kitts and Nevis</option>
            <option value="LC">Saint Lucia</option>
            <option value="MF">Saint Martin (French part)</option>
            <option value="PM">Saint Pierre and Miquelon</option>
            <option value="VC">Saint Vincent and the Grenadines</option>
            <option value="WS">Samoa</option>
            <option value="SM">San Marino</option>
            <option value="ST">Sao Tome and Principe</option>
            <option value="SA">Saudi Arabia</option>
            <option value="SN">Senegal</option>
            <option value="RS">Serbia</option>
            <option value="SC">Seychelles</option>
            <option value="SL">Sierra Leone</option>
            <option value="SG">Singapore</option>
            <option value="SX">Sint Maarten (Dutch part)</option>
            <option value="SK">Slovakia</option>
            <option value="SI">Slovenia</option>
            <option value="SB">Solomon Islands</option>
            <option value="SO">Somalia</option>
            <option value="ZA">South Africa</option>
            <option value="GS">South Georgia and the South Sandwich Islands</option>
            <option value="SS">South Sudan</option>
            <option value="ES">Spain</option>
            <option value="LK">Sri Lanka</option>
            <option value="SD">Sudan</option>
            <option value="SR">Suriname</option>
            <option value="SJ">Svalbard and Jan Mayen</option>
            <option value="SZ">Swaziland</option>
            <option value="SE">Sweden</option>
            <option value="CH">Switzerland</option>
            <option value="SY">Syrian Arab Republic</option>
            <option value="TW">Taiwan, Province of China</option>
            <option value="TJ">Tajikistan</option>
            <option value="TZ">Tanzania, United Republic of</option>
            <option value="TH">Thailand</option>
            <option value="TL">Timor-Leste</option>
            <option value="TG">Togo</option>
            <option value="TK">Tokelau</option>
            <option value="TO">Tonga</option>
            <option value="TT">Trinidad and Tobago</option>
            <option value="TN">Tunisia</option>
            <option value="TR">Turkey</option>
            <option value="TM">Turkmenistan</option>
            <option value="TC">Turks and Caicos Islands</option>
            <option value="TV">Tuvalu</option>
            <option value="UG">Uganda</option>
            <option value="UA">Ukraine</option>
            <option value="AE">United Arab Emirates</option>
            <option value="GB">United Kingdom</option>
            <option value="US">United States</option>
            <option value="UM">United States Minor Outlying Islands</option>
            <option value="UY">Uruguay</option>
            <option value="UZ">Uzbekistan</option>
            <option value="VU">Vanuatu</option>
            <option value="VE">Venezuela, Bolivarian Republic of</option>
            <option value="VN">Viet Nam</option>
            <option value="VG">Virgin Islands, British</option>
            <option value="VI">Virgin Islands, U.S.</option>
            <option value="WF">Wallis and Futuna</option>
            <option value="EH">Western Sahara</option>
            <option value="YE">Yemen</option>
            <option value="ZM">Zambia</option>
            <option value="ZW">Zimbabwe</option>
          </select>
          </div>
          <v-btn v-if="city.length && countryCode.length > 0" style="color: white" color="#4767ad" depressed large @click='gettingData()'>Find</v-btn>
        </v-flex>
      </v-layout>
    </v-container>



    <div class="jumbotron" v-for='item in cities'>
      <h1 class="display-4">{{item.name}}</h1>
      <p class="lead">Country: {{item.country}}</p>
    </div>

    
    <div v-if="loading">
      <div class="test">
        <div class="container">
         <div class="pseudo pseudo-1 right today" @click="scroll_right($event)" v-if="today[0].length > 1"></div>
          <div class="row scrolling" id="scrolling-1">
            <div class="col-sm-12 col-md col-lg small"  v-for="(item,i) in today[0]" :key="i">
              
              <div class="card"
              :style="changeBackgroundImage(item)">
              <div class="card-img-top sprite" :style="changeBakcgroundPosition(item)"> </div>
              <div class="card-body">
                <h3 class="card-title">Today</h3>
                <h3 class="card-title time">{{formattingTime(item)}}</h3>
                <hr>
                <p class="card-text">Weather: {{item.weather[0].description}}</p>
                <p class="card-text">Temperature: {{kelvinToCelsius(item)}} °C</p>
                <div class="bottom">
                <p class="wind">Wind: {{item.wind.speed}}m/s</p>
                <p class="humidity">Humidity: {{item.main.humidity}}%</p>
                </div>

              </div>
            </div>
            </div>
             
          </div>
         
  <div class="pseudo pseudo-1 left today"  @click="scroll_left($event)" v-if="today[0].length > 1"></div>
        </div>
      
      </div>

      <div class="test">
        <div class="container">
               <div class="pseudo pseudo-2 right" @click="scroll_right($event)" v-if="tomorrow[0].length > 4"></div>    

          <div class="row scrolling" id="scrolling-2">
            
            <div class="col-sm-12 col-md-6 col-lg-3 small"  v-for="(item,i) in tomorrow[0]" :key="i">
               
              <div class="card"
              :style="changeBackgroundImage(item)">
              <div class="card-img-top sprite" :style="changeBakcgroundPosition(item)"> </div>
              <div class="card-body">
                <h3 class="card-title">Tomorrow</h3>
                <h3 class="card-title time">{{formattingTime(item)}}</h3>
                <hr>
                <p class="card-text">Weather: {{item.weather[0].description}}</p>
                <p class="card-text">Temperature: {{kelvinToCelsius(item)}} °C</p>
                <div class="bottom">
                <p class="wind">Wind: {{item.wind.speed}}m/s</p>
                <p class="humidity">Humidity: {{item.main.humidity}}%</p>
                </div>
              </div>
            </div>
             
            </div>

          </div>
          <div class="pseudo pseudo-2 left" @click="scroll_left($event)" v-if="tomorrow[0].length > 4"></div>
        </div>
      </div>
   

          <div class="test">
        <div class="container">
             <div class="pseudo pseudo-3 right" @click="scroll_right($event)" v-if="twoDays[0].length > 4"></div>             

          <div class="row scrolling" id="scrolling-3">
            <div class="col-sm-12 col-md-6 col-lg-3 small"  v-for="(item,i) in twoDays[0]" :key="i">
                  
              <div class="card"
              :style="changeBackgroundImage(item)">
              <div class="card-img-top sprite" :style="changeBakcgroundPosition(item)"> </div>
              <div class="card-body">
                <h3 class="card-title">The day after</h3>
                <h3 class="card-title time">{{formattingTime(item)}}</h3>
                <hr>
                <p class="card-text">Weather: {{item.weather[0].description}}</p>
                <p class="card-text">Temperature: {{kelvinToCelsius(item)}} °C</p>
                <div class="bottom">
                <p class="wind">Wind: {{item.wind.speed}}m/s</p>
                <p class="humidity">Humidity: {{item.main.humidity}}%</p>
                </div>
              </div>
            </div>
             
            </div>
          </div>
          <div class="pseudo pseudo-3 left" @click="scroll_left($event)" v-if="twoDays[0].length > 4"></div>
        </div>
      </div>

    </div>
    <div v-else>
      {{errorMessage}}

    </div>
    
  </div>
</template>

<script>
import axios from 'axios';
import moment from 'moment';

export default {
  name: 'home',
  data() {
    return {
      dates: [],
      city: [],
      cities: [],
      country: '',
      today: [],
      tomorrow: [],
      twoDays: [],
      loading: false,
      error: false,
      errorMessage: '',
      countryCode: ''
    }
  },

  methods: {
    gettingData() {
      const self = this;
      this.loading = true;

      axios
      .get('http://api.openweathermap.org/data/2.5/forecast?q='+self.city+','+self.countryCode+'&appid=49f042b7a77ab562cf7c2fd0f68eee77')
      .then(response => {
        self.cities.push(response.data.city)

        //filter date === today---------------------------------------------
        var todayData = response.data.list.filter(function (el) {
          //starting filter
          var givenData = moment(el.dt_txt).format("YYYY-MM-DD");
          var givenDataString = JSON.stringify(givenData)
          console.log(givenData)
          var today = moment(new Date()).format("YYYY-MM-DD");
          var todayString = JSON.stringify(today)
          return givenDataString == todayString
        });
        self.today.push(todayData);


  
         //filter date === tomorrow--------------------------------------
        var tomorrowData = response.data.list.filter(function (el) {
          //starting filter
          var day = new Date();
          var result = new Date(day);
          var tomorrow = result.setDate(day.getDate()+1);
          var tomorrowMoment = moment(tomorrow).format("YYYY-MM-DD");
          var tomorrowString = JSON.stringify(tomorrowMoment)
          var givenData = moment(el.dt_txt).format("YYYY-MM-DD");
          var givenDataString = JSON.stringify(givenData)

          return givenDataString == tomorrowString
        })

        self.tomorrow.push(tomorrowData);



        //filter date === day after tomorrow------------------------------
        var twoDaysData = response.data.list.filter(function (el) {
          //starting filter
          var day = new Date();
          var result = new Date(day);
          var twoDays = result.setDate(day.getDate()+2);
         
          var twoDaysMoment = moment(twoDays).format("YYYY-MM-DD");
          var twoDaysString = JSON.stringify(twoDaysMoment)
          var givenData = moment(el.dt_txt).format("YYYY-MM-DD");
          var givenDataString = JSON.stringify(givenData)

          return givenDataString == twoDaysString
        })
        self.twoDays.push(twoDaysData)
      }).catch(error => {
        console.log(error)
        self.loading = false
        self.errorMessage = 'City not found please try again'
      })
      this.today = []
      this.tomorrow = []
      this.twoDays = []
      this.cities = []
    },
    changeBakcgroundPosition(item) {
      if(item.weather[0].main === 'Clear') {
        return {
          backgroundPosition: '-130px -17px'
        }
      }
       if(item.weather[0].main === 'Clouds') {
        return {
          backgroundPosition: '-28px -139px'
        }
      }
       if(item.weather[0].description === 'light rain') {
        return {
          backgroundPosition: '-28px -17px'
        }
      }
      if(item.weather[0].description === 'moderate rain') {
        return {
          backgroundPosition: '-232px -16px'
        }
      }

      if(item.weather[0].description === 'light snow') {
        return {
          backgroundPosition: '-130px 247px'
        }
      }


    },

    changeBackgroundImage(item) {
      var dateString = JSON.stringify(item.dt_txt);
      var justTime = dateString.split(" ").pop()

      if(justTime > "08:00:00" && justTime < '17:00:00') {
        return {
          background: '#00ccff'
        }
      } else {
        return {
           background: 'rgb(14, 52, 82)',
           color: 'white'
        }
       
      }
    },
    formattingDate(item) {
      var dateFormatted = moment(item.dt_txt).format("DD-MM-YYYY");
      return dateFormatted
    },

    formattingTime(item) {
      var dateFormatted = moment(item.dt_txt).format("h:mm a");
      return dateFormatted
    },

  scroll_right(event) {
    var classEl = event.target.className
     var container;
    if(classEl === "pseudo pseudo-1 right") {
      container =  document.getElementById('scrolling-1');
    }

    if(classEl === "pseudo pseudo-2 right") {
      container =  document.getElementById('scrolling-2');

    }

    if(classEl === "pseudo pseudo-3 right") {
      container =  document.getElementById('scrolling-3');

    }
   
    var scrollAmount = 0;
    var slideTimer = setInterval(function(){
        container.scrollLeft += 30;
        scrollAmount += 10;
        if(scrollAmount >= 100){
            window.clearInterval(slideTimer);
        }
    }, 25);

  },
  
  scroll_left(event) {
     var classEl = event.target.className
     var container;
    if(classEl === "pseudo pseudo-1 left") {
      container =  document.getElementById('scrolling-1');

    }

    if(classEl === "pseudo pseudo-2 left") {
      container =  document.getElementById('scrolling-2');

    }

    if(classEl === "pseudo pseudo-3 left") {
      container =  document.getElementById('scrolling-3');

    }
    var scrollAmount = 0;
    var slideTimer = setInterval(function(){
        container.scrollLeft -= 30;
        scrollAmount += 10;
        if(scrollAmount >= 100){
            window.clearInterval(slideTimer);
        }
    }, 25);

  },
    kelvinToCelsius(item) {
    if (item.main.temp < (0)) {
      return 'below absolute zero (0 K)';
    } else {
      var celsius = item.main.temp-273.15;
      var celsiusNoDec = Math.trunc( celsius );
      return celsiusNoDec
    }

}

   

  },
  computed: {
    
  }
}
</script>
<style lang="scss">

.small {
 @media only screen and (max-width: 575px) {
    flex: 0 0 100%;
 }
 
}

.v-btn__content {
  color: black !important;
}

.sprite {
  position: absolute;
  width: 110px;
  height: 110px;
  border-radius: 50%;
  left: 50%;
  top: 50%;
  transform: translateY(-50%);
  transform: translateX(-50%);
  background: url('https://cmkt-image-prd.global.ssl.fastly.net/0.1.0/ps/2163737/580/386/m1/fpnw/wm0/craetive-market-image-.png?1485043762&s=94d2489c6e978820161f738ad70f1577');
}



.v-btn__content {
    color: white !important;
    font-weight: bold;
    letter-spacing: 1px
}

.card{
  height: 400px;
}

.row {
  flex-wrap: nowrap !important;
}

.scrolling {
  overflow-x: scroll;
  max-width: 100%; 
  margin: 0 auto;
}

.pseudo {
  width: 20px;
  height: 20px;
  position: absolute;
  cursor: pointer;
  display: inline-block;
  border-right: 4px solid black;
  border-bottom: 4px solid black;
  width: 10px; height: 10px;

}

.right {
  top: 50%;
  transform: translateY(-50%) rotate(-47deg);
  right: -15px;
  @media only screen and (max-width: 575px) {
    right: 10px
  }
}

.left {
   top: 50%;
  transform: translateY(-50%) rotate(-225deg);
  left: -15px; 

    @media only screen and (max-width: 575px) {
    left: 10px
  }
}

.today {
  @media only screen and (min-width: 768px) {
    display: none;
  }
}

.container {
  position: relative;
}

.bottom {
  display: flex;
  justify-content: space-around;
  flex-wrap: nowrap;
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
}
.list-enter-active, .list-leave-active {
  transition: all 1s;
}
.list-enter, .list-leave-to /* .list-leave-active below version 2.1.8 */ {
  opacity: 0;
  transform: translateY(30px);
}

.styled-select {
   background: url(http://i62.tinypic.com/15xvbd5.png) no-repeat 96% 0;
   margin: 0 auto;
   margin-bottom: 20px;
   margin-top: 20px;
   height: 29px;
   overflow: hidden;
   width: 240px;
}

.styled-select select {
   background: transparent;
   border: none;
   font-size: 14px;
   height: 29px;
   padding: 5px; /* If you add too much padding here, the options won't show in IE */
   width: 268px;
}

.styled-select.slate {
   background: url(http://i62.tinypic.com/2e3ybe1.jpg) no-repeat right center;
   height: 34px;
   width: 240px;
}

.styled-select.slate select {
   border: 1px solid #ccc;
   font-size: 16px;
   height: 34px;
   width: 268px;
}


</style>


