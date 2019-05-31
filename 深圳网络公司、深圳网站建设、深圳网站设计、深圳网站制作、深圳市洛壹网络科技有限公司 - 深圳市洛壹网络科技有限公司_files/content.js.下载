$(function() {
	// 浏览器升级提示
	var userAgent = navigator.userAgent; //取得浏览器的userAgent字符串  
    var reIE = new RegExp("MSIE (\\d+\\.\\d+);");  
    reIE.test(userAgent);  
    var fIEVersion = parseFloat(RegExp["$1"]);  
    if(fIEVersion == 7) { 
       $(".yy").addClass('cur00');$(".yy-box").addClass('cur00');
    }else  { 
       $(".yy").removeClass('cur00');$(".yy-box").removeClass('cur00');
    }

    // 兼容样式的修改
	$(".ly-header-top ul li:last").css("borderRight","0");
	$(".nav li a:last").css("marginRight","0");
	$(".solution-ul li:last").css("marginRight","0");
	$(".honor-ul li:last").css("marginRight","0");
	$(".zhuanshu ul li:odd").css("marginRight","0");
	$(".footer-ul li:odd").css("marginRight","0");
	$(".box-lei ul li:last").css("marginRight","0");
	$(".a-div-5 ul li:nth-child(5n)").css("marginRight","0");
	$(".number:last").css("borderBottom","0");
	$(".number:last").css("paddingBottom","70px");
	$(".slogan ul li:last").css("marginRight","0");
	$(".yghd ul li:odd").css("float","right");
	$(".n-nav li:last").css("borderBottom","0");
	

	$(document).ready(function() {

		// 导航栏滑动
		$(".nav li").hover(function(){
			$(this).children(".submenu").stop().slideToggle();
			return false;
		});

		// 广告播放
		function scrollTxt(){
		    var controls={}, 
		        values={},
		        t1 = 1000, /*播放动画的时间*/
		        t2 = 3000, /*播放时间间隔*/
		        si;
		    controls.rollWrap = $(".cont-div");
		    controls.rollWrapUl = controls.rollWrap.children();
		    controls.rollWrapLIs = controls.rollWrapUl.children();
		    values.liNums = controls.rollWrapLIs.length;
		    values.liHeight = controls.rollWrapLIs.eq(0).height();
		    values.ulHeight = controls.rollWrap.height();
		    this.init = function() {
		        autoPlay();
		        pausePlay();
		    }
		    /*滚动*/
		    function play(){
		        controls.rollWrapUl.animate({"margin-top" : "-"+values.liHeight}, t1, function() {
		            $(this).css("margin-top" , "0").children().eq(0).appendTo($(this));
		        });
		    }
		    /*自动滚动*/
		    function autoPlay() {
		        /*如果所有li标签的高度和大于.cont-div的高度则滚动*/
		        if(values.liHeight*values.liNums > values.ulHeight){
		            si=setInterval(function() {
		                play();
		            },t2);
		        }
		    }
		    /*鼠标经过ul时暂停滚动*/
		    function pausePlay() {
		        controls.rollWrapUl.on({
		            "mouseenter":function(){
		                clearInterval(si);
		            },
		            "mouseleave":function(){
		                autoPlay();
		            }
		        });
		    }
		}
		new scrollTxt().init();

		$(window).scroll(function(){
			if($(window).scrollTop() > 40){
				$('.ly-header-b').addClass('cur0');
			}else{
				$('.ly-header-b').removeClass('cur0');
			};
		})

		//荣誉滚动
		function rongyuscroll(){
			var scrtime;
			$(".honor-div").hover(function(){
				clearInterval(scrtime);
			},function(){
			scrtime = setInterval(function(){
				var $ul = $(".honor-div ul");
				var liHeight = $ul.find("li:last").height();
				$ul.animate({marginTop : -liHeight + 0 + "px"},500,function(){
				$ul.find("li:first").appendTo($ul)
				$ul.css({marginTop:0});
				});
			},2000);
			}).trigger("mouseleave");
		}
		rongyuscroll();

		$(".bankuai li").each(function(){
	        $(this).hover(function(){
	            $(this).find(".mr").addClass("a-active");
	            $(this).find('.pic1').stop().animate({right:'-100%'},300);
	            $(this).find('.pic2').stop().animate({left:'0'},300);
	            $(this).find('.text1').stop().animate({left:'-100%'},300);
	            $(this).find('.text2').stop().animate({right:'0'},300);
	        },function(){
	            $(this).find(".mr").removeClass("a-active");
	            $(this).find('.pic1').stop().animate({right:'0'},300);
	            $(this).find('.pic2').stop().animate({left:'-100%'},300);
	            $(this).find('.text1').stop().animate({left:'0'},300);
	            $(this).find('.text2').stop().animate({right:'-100%'},300);
	        });
	    });

	    // 新闻资讯
	    $(".new-nav p").hover(function() {
	    	$(this).addClass('no').siblings().removeClass('no');
	    	var i = ($(this).index());
	    	$('.news .box p').removeClass('x0');
	    	$('.news .box p').removeClass('x1');
	    	$('.news .box p').removeClass('x2');
	    	$('.news .box p').addClass('x' + i);
        	$('.new-box .N_content').eq(i).show().siblings().hide();
	    })

	    // 我们的团队
	    var b = $(".team_Mlist li").length;$(".team_Mlist ul").width(1124*b);
		var c = 1;
		$(".team_r").click(function(){
			if(c<b){
				var d=$(".team_Mlist ul");
				d.stop(true,true).animate({marginLeft:-c*140},800);
				$(".team_Mlist ul li").eq(c).addClass("team_on").siblings().removeClass("team_on");
				var e=$(".team_Mlist ul li").eq(c).attr("data-ask");
				$(".team_ask").html(e);
			c++}
		});
		$(".team_l").click(function(){
			if(c>1){
				var d=$(".team_Mlist ul");
				d.stop(true,true).animate({marginLeft:-(c-2)*140},800);
				$(".team_Mlist ul li").eq(c-2).addClass("team_on").siblings().removeClass("team_on");
				var e=$(".team_Mlist ul li").eq(c-2).attr("data-ask");
				$(".team_ask").html(e);
			c--}
		});
		$(".team_Mlist li").eq(3).addClass("team_on");
		var a=$(".team_Mlist li:eq(3)").attr("data-ask");
		$(".team_ask").html(a);
		$(".team_Mlist li").hover(function(){
			var d=$(this).attr("data-ask");
			$(".team_ask").html(d);
			$(this).addClass("team_on").siblings().removeClass("team_on")
		});

		// 推荐案例 点击切换
		$(".kuang-a a ").on("click",function() {
			$(this).addClass("cur3").siblings().removeClass("cur3");
			var k = $(this).index();
			$(".kuang .kuang-div").eq(k).show().siblings().hide();
		})

		// 案例详情
		$(".middle ul li ").on("click",function() {
			$(this).addClass("cur4").siblings().removeClass("cur4");
			var m = $(this).index();
			$('.item .pp').eq(m).addClass("cur").siblings().removeClass("cur");
			$('.item .pp').eq(m).children('.img').css('top',"0px");
		})
		
		//百度口碑滚动
		function baiduscroll(){
			var scrtime;
			$(".rs").hover(function(){
				clearInterval(scrtime);
			},function(){
			scrtime = setInterval(function(){
				var $ul = $(".rs ul");
				var liHeight = $ul.find("li:last").height();
				$ul.animate({marginTop : -liHeight + 0 + "px"},1000,function(){
				$ul.find("li:first").appendTo($ul)
				$ul.css({marginTop:0});
				$ul.find("li:first").fadeIn(1000);
				});
			},3000);
			}).trigger("mouseleave");
		}
		baiduscroll();

		// 企业邮箱弹窗
		$(".index_product_buy_opt_btn a").on("click",function() {
			$(".baojia_warp").show();
		})
		$(".close").on("click",function() {
			$(".baojia_warp").hide();
		})
		// 建站方案切换
        $(".w_fl .w_fl-box").hover(function() {
            var i = $(this).index();
            $(".w_grid ul").eq(i).fadeIn().siblings().fadeOut();
        })
        // 建站问题
        $(".list-8big li p.txt2 a").on("click",function() {
            var i = $('.list-8big li p.txt2 a').index(this);
            $('.des1').removeClass('on');
            $(".list-8big li").eq(i).children('.des1').addClass('on').siblings().removeClass('on');
        })
	})
})
