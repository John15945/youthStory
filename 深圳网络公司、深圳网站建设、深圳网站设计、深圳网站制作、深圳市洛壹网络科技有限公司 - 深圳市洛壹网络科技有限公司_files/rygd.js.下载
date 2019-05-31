$(function() {
	// 我们的优势数字递增
    var options = {
		useEasing : true, 
		useGrouping : true, 
		separator : '', 
		decimal : '', 
		prefix : '', 
		suffix : '' 
	};
	var demo = new CountUp("myTargetElement", 0, 30, 0, 2.5, options);
	var demo2 = new CountUp("myTargetElement2", 0, 95, 0, 2.5, options);
	var demo3 = new CountUp("myTargetElement3", 0, 6, 0, 2.5, options);
	var demo4 = new CountUp("myTargetElement4", 0, 1500, 0, 2.5, options);
	$(window).scroll(function(){
		var o = $('.superiority').offset().top - $(window).scrollTop();
		var p = $('.honor').offset().top - $(window).scrollTop();
		if(o <= 800){
			demo.start();
			demo2.start();
			demo3.start();
			demo4.start();
		}
		if (p <= 770) {
			$('.honor-ul').addClass('cur00');
		}
		if($(window).scrollTop() > 40){
			$('.ly-header-b').addClass('cur0');
		}else{
			$('.ly-header-b').removeClass('cur0');
		};
	})

}) 