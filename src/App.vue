<template>
  <div id="app">
    <div id="grad">
      <h1>Flyby</h1>
      <h2>Welcome</h2>
      <img src="./assets/flyby-drone.jpg" width="700px" height="400px">
      <h3>Something something drones something something immune system </h3>
    </div>
    <div >
      <h2 id="grad">
        Our values
      </h2>
      <div id="ol">
      <ol>
        <li>Do not give opinions or advice unless you are asked.</li>
        <li>Do not tell your troubles to others unless you are sure they want to hear them.</li>
        <li>When in another's home, show them respect or else do not go there.</li>
        <li>If a guest in your home annoys you, treat him cruelly and without mercy.</li>
        <li>Do not make sexual advances unless you are given the mating signal.</li>
        <li>Do not take that which does not belong to you unless it is a burden to the other person and they cry out to be relieved.</li>
        <li>Acknowledge the power of magic if you have employed it successfully to obtain your desires. If you deny the power of magic after having called upon it with success, you will lose all you have obtained.</li>
        <li>Do not complain about anything to which you need not subject yourself.</li>
        <li>Do not harm little children.</li>
        <li>Do not kill non-human animals unless you are attacked or for your food.</li>
        <li>When walking in open territory, bother no one. If someone bothers you, ask him to stop. If he does not stop, destroy him.</li>
      </ol>
      </div>
    </div>
    <div>
      <h2 id="grad">Meet the Team</h2>
      <div id="flex">
        <div>
          <h3>Ayden Chubbic, The Eastern Moon</h3>
          <img src = "./assets/alan.png" width ="400px" height = "330px">
        
        </div>
        <div>
          <h3>Alan Brilliant, Herald of Awakening</h3>
          <img src = "./assets/ayden.png" width ="410px" height = "330px">
          
        </div>

        <div>
          <h3>Arnold, Intern</h3>
          <img src = "./assets/arnold.png" width ="450px" height = "330px">
          
        </div>
      </div>
      
      

    </div>
  </div>
</template>

<script>

export default {
 
}
</script>

<style>

#app {
  text-shadow: white 0px 0px 10px;
  
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
#ol {
  text-align: left;
}
h3 {
  margin: 40px 20px 20px;
}

#grad{
  background: rgb(0,212,255);
  background: linear-gradient(90deg, rgba(0,212,255,1) 23%, rgba(9,9,119,1) 93%, rgba(2,0,36,1) 100%); 
}

#flex{

  margin: 40px 40px 40px;
  /* padding: 40px 40px 40px; */
  display: flex;
  flex-direction: row;
  justify-content: space-around
  
}
</style>
