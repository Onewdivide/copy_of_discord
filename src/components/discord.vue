<template>
  <mainContainer>

    <navbar>
      <leftNavbar>
        <i class="fab fa-discord discordlogo"></i>
        <div>Download</div>
        <div @mouseover="toggleShowPopup('gamesPopup')" @mouseout="toggleShowPopup('gamesPopup')">Games <i class="fas fa-angle-down"></i></div>
        <div>Jobs</div>
        <div @mouseover="toggleShowPopup('developerPopup')" @mouseout="toggleShowPopup('developerPopup')">Developers <i class="fas fa-angle-down"></i></div>
        <div @mouseover="toggleShowPopup('communityPopup')" @mouseout="toggleShowPopup('communityPopup')">Community <i class="fas fa-angle-down"></i></div>
        <div @mouseover="toggleShowPopup('helpPopup')" @mouseout="toggleShowPopup('helpPopup')">Support <i class="fas fa-angle-down"></i></div>
      </leftNavbar>

      <rightNavbar>
        <contactLogo>
        <i class="fab fa-twitter contactlogo"></i>
        <i class="fab fa-facebook contactlogo"></i>
        <i class="fab fa-instagram contactlogo"></i>
        </contactLogo>
        
        <loginBtn>Login</loginBtn>

        <language>
          <div class="leftBorder_language"></div>
          <i class="fas fa-language languageLogo"></i>
          <i class="fas fa-angle-down"></i>
        </language>
      </rightNavbar>
    </navbar>

    <mainBody>
      <headerInBody>
      <mainHeader>
        It's time to ditch Skype and TeamSpeak.
      </mainHeader>
      <descriptionHeader>
        <div>
          All-in-one voice and text chat for gamers that's free, secure, and works on both your desktop and phone.
        </div>
        <div>
          Stop paying for TeamSpeak servers and hassling with Skype. Simplify your life.
        </div>
      </descriptionHeader>
      <buttonArea>
        <div class="downloadBtn">Download for Windows</div>
        <div class="openBrowserBtn">Open Discord in your Browser</div>
      </buttonArea>
      </headerInBody>
      <bodyInBody>
        <div style="position:relative;">
       <img class="mainCom" src='../assets/maincom.svg'>
       <img class="com" src="../assets/com.svg">
       <img class="joyStick" src="../assets/joyStick.svg">
       <img class="iphone" src="../assets/iphone.svg">
       <img class="android" src="../assets/android.svg">
       <img id="misteryBox" v-on:click="randomThingsFromMisteryBox()" class="misteryBox" src="../assets/misteryBox.svg">
       <img id="coin" class="thingsInMisteryBox" src="../assets/coin.svg">
       <img id="redFlower" class="thingsInMisteryBox" src="../assets/redFlower.svg">
       <img id="redMushroom" class="thingsInMisteryBox" src="../assets/redMushroom.svg">
       <img id="star" class="thingsInMisteryBox" src="../assets/star.svg">
       <img class="thingsUpDownCoin1" src="../assets/coin.svg">
       <img class="thingsUpDownBomb" src="../assets/bomb.svg">
       <img class="thingsUpDownCoin2" src="../assets/coin.svg">
        </div>
      </bodyInBody>
    </mainBody>

    <mainFooter>
      <about>
        <colDesctiption>
        <i class="fab fa-discord discordlogo"></i>
        </colDesctiption>

        <colDesctiption>
        <div class="headerIncolDesctiption">Product</div>
        <div class="descriptionInColDescrition">Download</div>
        <div class="descriptionInColDescrition">Branding</div>
        <div class="descriptionInColDescrition">Nitro</div>
        <div class="descriptionInColDescrition">Game Directory</div>
        </colDesctiption>

        <colDesctiption>
        <div class="headerIncolDesctiption">Developers</div>
        <div class="descriptionInColDescrition">Application</div>
        <div class="descriptionInColDescrition">Documentation</div>
        <div class="descriptionInColDescrition">Verification</div>
        <div class="descriptionInColDescrition">Rich Presense</div>
        </colDesctiption>

        <colDesctiption>
        <div class="headerIncolDesctiption">Resources</div>
        <div class="descriptionInColDescrition">Help & Support</div>
        <div class="descriptionInColDescrition">Guidelines</div>
        <div class="descriptionInColDescrition">Feedback</div>
        <div class="descriptionInColDescrition">Term</div>
        <div class="descriptionInColDescrition">Privacy</div>
        <div class="descriptionInColDescrition">Status</div>
        </colDesctiption>

        <colDesctiption>
        <div class="headerIncolDesctiption">Company</div>
        <div class="descriptionInColDescrition">About</div>
        <div class="descriptionInColDescrition">Blog</div>
        <div class="descriptionInColDescrition">Jobs</div>
        </colDesctiption>

        <colDesctiption>
        <div class="headerIncolDesctiption">More</div>
        <div class="descriptionInColDescrition">Partners</div>
        <div class="descriptionInColDescrition">HypeSquad</div>
        <div class="descriptionInColDescrition">Merch Store</div>
        <div class="descriptionInColDescrition">Press Inquiries</div>
        <div class="descriptionInColDescrition">Open Source</div>
        </colDesctiption>
      </about>
      <signUp>
        <div>
          <div class="headerInsignUpArea">Ready to try Discord? It's free!</div>
          <div class="descriptionInsignUpArea">JOIN OVER 150 MILLION PLAYERS TODAY</div>
        </div>

        <div class="signUpBtn" id="test">
          Sign Up Now
        </div>

      </signUp>
    </mainFooter>

  <div id="gamesPopup" class="popUpUndergames" >
    <div>Nitro</div>
    <div>Games Directory</div>
  </div>

  <div id="developerPopup" class="popUpUnderdeveloper">
    <div>Rich Presence</div>
    <div>Verification</div>
    <div>Developer Portal</div>
    <div>Documentation</div>
  </div>

  <div id="communityPopup" class="popUpUndercommunity">
    <div>Rich Presence</div>
    <div>Verification</div>
    <div>Developer Portal</div>
    <div>Documentation</div>
  </div>

  <div id="helpPopup" class="popUpUnderhelp">
    <div>Rich Presence</div>
    <div>Verification</div>
    <div>Developer Portal</div>
    <div>Documentation</div>
  </div>

  </mainContainer>
  
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  methods:{
    toggleShowPopup(popupID){
      var popUp = document.getElementById(popupID)
      document.getElementById(popupID).classList.toggle('visibleForToggle')
    },
    randomThingsFromMisteryBox(){
      document.getElementById("misteryBox").classList.toggle("animationShakeBox")
      var thing = Math.floor(Math.random() * 4);
      if(thing == 0){
        document.getElementById("redFlower").classList.toggle("animationToTopOfBox")
      }else if(thing == 1){
        document.getElementById("coin").classList.toggle("animationToTopOfBox")
      }else if(thing == 2){
        document.getElementById("redMushroom").classList.toggle("animationToTopOfBox")
      }else{
        document.getElementById("star").classList.toggle("animationToTopOfBox")
      }

      console.log(thing)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../sass/main.scss';


.mainCom{
  position: absolute;
  margin-left:30%;
  bottom: -550px;
  z-index: 2;
}

.com{
  position: absolute;
  margin-left: 50%;
  bottom: -550px;
  z-index: 3;
}

.joyStick{
  position: absolute;
  margin-left: 33%;
  bottom: -550px;
  z-index: 3;
}

.iphone{
  position: absolute;
  margin-left: 23%;
  bottom: -550px;
  z-index: 3;
}

.android{
  position: absolute;
  margin-left: 13%;
  bottom: -550px;
  z-index: 3;
}

.misteryBox{
  position: absolute;
  margin-left:32%;
  bottom: -100px;
  z-index: 1;
  cursor: pointer;
}

.thingsInMisteryBox{
  position: absolute;
  margin-left:32.5%;
  bottom: -100px;
  z-index: 0;
}

.thingsUpDownCoin1{
  position: absolute;
  margin-left:20%;
  bottom: -230px;
  z-index: 1;
  animation: upDown 3s infinite 0.3s;
}

.thingsUpDownBomb{
  position: absolute;
  margin-left:17%;
  bottom: -190px;
  z-index: 0;
  animation: upDown 3s infinite 0s;
}

.thingsUpDownCoin2{
  position: absolute;
  margin-left:70%;
  bottom: -100px;
  z-index: 1;
  animation: upDown 3s infinite 0.7s;
}


h3 {
  // margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  // margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
