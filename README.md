<script>
var Animal = function(n, s, f) {
  this.name= n;
  this.speed= s;
  this.focus = f;
  this.position= 0;
  this.report= function() {
    return this.name + " is at " + this.position;
  };
  this.run = function() {
    if(this.focus > (Math.random() * 10)) {
        this.position += this.speed;
    }
  };
}

var turtle = new Animal("Timmy the Turtle", 2, 8),
    rabbit = new Animal("Mopsy the Rabbit", 8, 2);
    pug = new Animal("Prince the Pug",0,0)

var distance= 30;

while(turtle.position < distance && rabbit.position < distance && pug.position < distance) {
    turtle.run();
    rabbit.run();
    pug.run();

};
var userChoice = prompt("Lets make a bet on whose gonna win... Would you like to choose Timmmy the Turtle, Prince the Pug or Mopsy the Rabbit??");
alert(turtle.report());
alert(rabbit.report());
alert(pug.report());
alert("Looks like prince fell asleep before the race :/")
if (turtle.position > rabbit.position) {
  alert("The turtle won... you cannot underestimate the underdog!!!$$$$$$ Prince never had a chance")
}
else {
  alert("The rabbit won....I guess this game isn't like the stories$$$$$ Prince never had a chance")
}




</script>
