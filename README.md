<!doctype html>
<html>
<head>
<meta charset="utf-8">
<title>Untitled Document</title>

<style>
*{
	box-sizing:border-box;
-webkit-box-sizing:border-box;	
margin:0px;
padding:0px;
}
bodt,html{
height:100%;

}

section{
background:red;	
width:100%;
border-bottom:2px solid;
height:400px;
float:left;
overflow:hidden;
}

.daniel{
background:#000;	
}
.daniel1{
background:green;	
}
.daniel2{
background:blue;	
}
.container{
width:1200px;
margin:0 auto;
}
.div_one{
width:100%;
float:left;	
height:100%;
position:relative;

}
.div_one_left{
width:50%;
float:left;
height:400px;
background:#fff;
	position:absolute;
	left:-1000px;
	 transition: all 1s ease-out;
 -webkit-transition: all 1s ease-out;
}
.div_one_right{
width:50%;
float:right;
height:400px;
background:green;
	position:absolute;
	right:-1000px;
	 transition: all 1s ease-out;
 -webkit-transition: all 1s ease-out;
}
.left_effect{
position:absolute;
left:0px;
top:0px;
  transition: all 1s ease-out;
 -webkit-transition: all 1s ease-out;
}
.right_effect{
position:absolute;
right:0px;
top:0px;
 transition: all 1s ease-out;
 -webkit-transition: all 1s ease-out;
}
.div_one_left_one{
width:33.33%;
height:400px;
left:-1000px;
position:absolute;
transition: all 1s ease-out;
 -webkit-transition: all 1s ease-out;
 background:blue;	
}
.div_one_left_two{
width:33.33%;
height:400px;
left:-1000px;
position:absolute;
transition: all 1s ease-out;
 -webkit-transition: all 1.4s ease-out;
 background:green;	
}
.div_one_left_three{
width:33.33%;
height:400px;
left:-1000px;
position:absolute;
transition: all 1s ease-out;
 -webkit-transition: all 1.8s ease-out;	
 background:#333;
}
.div_one_left_one_left{
left:0%;
transition: all 1s ease-out;
 -webkit-transition: all 0.5s ease-out;	
}
.div_one_left_two_center{
left:33.3%;
transition: all 1s ease-out;
 -webkit-transition: all 1s ease-out;	
}
.div_one_left_three_right{
left:66.6%;
transition: all 1s ease-out;
 -webkit-transition: all 1.5s ease-out;	
}
</style>
</head>
<body>
<section class="section_1">
</section>
<section class="section_2">
    <div class="container">
    	<div class="div_one">
        	<div class="div_one_left">
        		
            </div>
            <div class="div_one_right">
        
            </div>
        </div>
    </div>
</section>
<section class="section_3">
<div class="container">
    	<div class="div_one">
        	<div class="div_one_left_one">
        		
            </div>
            <div class="div_one_left_two">
        
            </div>
            <div class="div_one_left_three">
        
            </div>
        </div>
    </div>
</section>
<section class="section_4">

</section>
<section class="section_5">

</section>
<section class="section_5">

</section>
<section class="section_5">

</section>


</body>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.0/jquery.min.js"></script>

<script>
$(function(){
	$(window).scroll(function(){
		var scrl_value = $(window).scrollTop();
		var section1 = $(".section_2").offset().top;
		if(scrl_value+100 >= section1)
		{
			$(".div_one_left").addClass("left_effect");	
			$(".div_one_right").addClass("right_effect");
		}
		else
		{
			$(".div_one_left").removeClass("left_effect");	
			$(".div_one_right").removeClass("right_effect");
		}
		
		var section2 = $(".section_3").offset().top;
		if(scrl_value+100 >= section2)
		{
			$(".div_one_left_one").addClass("div_one_left_one_left");
			$(".div_one_left_two").addClass("div_one_left_two_center");
			$(".div_one_left_three").addClass("div_one_left_three_right");	
		}
		else
		{
			
			$(".div_one_left_one").removeClass("div_one_left_one_left");
			$(".div_one_left_two").removeClass("div_one_left_two_center");
			$(".div_one_left_three").removeClass("div_one_left_three_right");
		}
	})
})
</script>
</html>
