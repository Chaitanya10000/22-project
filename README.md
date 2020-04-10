# 22-project

//creating boxes

var box = createSprite(randomNumber(50,370),randomNumber(30,370),randomNumber(5,60),randomNumber(5,60));
box.setAnimation("box");
box.setCollider("rectangle", 10, 0, 200, 200, 90);
box.scale = 0.2;

//creating box group
var BoxGroup = createGroup();

function draw() {
  background("white");
  box.velocityY = 3;
  
  createEdgeSprites();
  box.collide(bottomEdge);
  
  //making more boxes
  if(keyDown("space")){
    box = createSprite(randomNumber(50,370),randomNumber(30,370),randomNumber(5,60),randomNumber(5,60));
    box.velocityY = 3;
    box.shapeColor = "#b97a57";
    BoxGroup.add(box);
 }
  drawSprites();
}
