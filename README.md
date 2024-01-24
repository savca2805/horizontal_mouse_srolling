horizontal mouse scrolling 

Everything should be clear here. Just paste the js code and insert your div and class parameters.

Everything should be clear here. Just paste the js code and insert your div and class parameters.
Save the entire page to yourself and open it in a browser for an example.

<html>
<head>
  <!-- for convenience, include the jquery library -->
  <script src = "https://www.tutorialspoint.com/jquery/jquery-3.6.0.js"></script>
  <script>
	  $(function(){
			/// optional value
			var scroll_step = 100;
			var scroll_div = $(".horizontal-menu")[0];
			$(document).on("wheel",".horizontal-menu", function(e){
				if(e.originalEvent.wheelDelta /120 > 0) {
					scroll_back(scroll_div);
				}else{
					scroll_forward(scroll_div);
				}
			});
			
		  function scroll_forward(scrolledElem, step=scroll_step){
			scrolledElem.scrollLeft = scrolledElem.scrollLeft + step;
		  }
		  function scroll_back(scrolledElem,step=100){
			scrolledElem.scrollLeft = scrolledElem.scrollLeft - step;
		  }
	  })   

  </script>
  <style>
	.horizontal-menu{
		margin:auto;
		width:200px;
		height:30px;
		overflow:auto;
	}
	.horizontal-menu span{
		padding:5px;
	}
  </style>
</head>
<body>
<div class="horizontal-menu">
	<nobr>
	  <span>one</span>
	  <span>two</span>
	  <span>three</span>
	  <span>four</span>
	  <span>five</span>
	  <span>six</span>
	  <span>seven</span>
	  <span>eiпре</span>
	  <span>nine</span>
	  <span>ten</span>
	</nobr>
</div>
</body>
