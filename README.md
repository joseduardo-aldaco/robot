float x=0;
float y=0;
float easing=0.01;

void setup()
{
  size (640,640);
}
void draw()
{
  robot();
  cir();
}
void robot()
{
  background(255);
  int targetY=mouseY;
  int targetX=mouseX;
  x+=(targetX-x)*easing;
  y+=(targetY-y)*easing;
  float dx=150;
  float dy=150;
  
  strokeWeight(1);
  fill(#3A3B39);
  stroke(#343B2C);
  rect(x-110,y-10,dx/2,dy/4);
  rect(x+40,y-10,dx/2,dy/4);
  
  strokeWeight(3);
  fill(#C1C1B7);
  noStroke();
  ellipse(x,y-100,dx/5,dy/5);
  stroke(1);
  fill(#84A06E);
  stroke(#657954);
  ellipse(x,y,dx,dy);
  stroke(1);
  fill(#C1C1B7);
  noStroke();
  ellipse(x,y-25,dx/2,dy/2);
  noStroke();
  fill(#4D0E10);
  ellipse(x,y-25,dx/3,dy/3);
  stroke(1);
  
   fill(#656667);
   stroke(#3B3C3E);
   smooth();
   strokeJoin(BEVEL);
   strokeWeight(5);
  rect(x-37,y+30,dx/2,dy/6);
  stroke(1);
}
void cir()
  {
    int targetY=mouseY;
    int targetX=mouseX;
    x+=(targetX-x)*easing;
    y+=(targetY-y)*easing;
 
    float dx=150;
    float dy=150;
    strokeWeight(3);
    noStroke();
    fill(#41430B);
    ellipse(x,y+105,dx,dy/4);
    fill(#656730);
    ellipse(x,y+125,dx/1.5,dy/4);
    fill(#41430B);
    ellipse(x,y+145,dx/2.5,dy/4);
    stroke(1);
  }
