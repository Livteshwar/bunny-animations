function Collide(ob1,ob2)
  {
    if(ob1!=null){
      var d= dist(ob1.position.x,ob1.position.y,ob2.position.x,ob2.position.y)

      if(d<=80){
        World.remove(world,fruit);
        fruit=null
        console.log(d)
        return true
      }
      else{
        return false
      }

    }

  }

  if(Collide(fruit,bunny)==true){
    bunny.changeAnimation("eating")
  }

  if(Collide(fruit,ground.body)==true){
    bunny.changeAnimation("crying")
  }