<html>

	<head>
		<meta charset="utf-8" />
		<title>巨藻载玻片</title>
		<meta name="Keywords" content="巨藻,锴国实业,载玻片" />
		<link rel="stylesheet" type="text/css" href="./css/bootstrap.min.css" />
		<link rel="stylesheet" type="text/css" href="./css/yuankustyle.css" />
		<script src="./js/jquery-1.10.2.min.js" type="text/javascript" charset="utf-8"></script>
		<script src="./js/bootstrap.min.js" type="text/javascript" charset="utf-8"></script>
		<script src="./js/jquery.easing.1.3.js" type="text/javascript" charset="utf-8"></script>
		<script src="./js/jquery.scrollbox.js" type="text/javascript" charset="utf-8"></script>

		<script type="text/javascript">
			function scTO(id) {
				var goTo = $(id).offset().top - 100;
				if (id == "#index") {
					$(".banner_content").hide();
				} else if (id == "#about") {
					$(".about_img img").hide();
				} else if (id == "#service") {
					$(".sev_img1").hide();
					$(".sev_img2").hide();
					$(".sev_img3").hide();
					$(".sev_img4").hide();
					$(".sev_img5").hide();
				}
				$("html, body").stop().animate({
					scrollTop: goTo
				}, 500, 'easeInExpo', function() {
					if (id == "#index") {
						$(".banner_content").slideDown("slow", 'easeOutBounce');
					} else if (id == "#about") {
						$(".about_img img").fadeIn("slow");
					} else if (id == "#service") {
						$(".sev_img1").slideDown("slow", 'easeOutBounce', function() {
							$(".sev_img2").slideDown("slow", 'easeOutBounce', function() {
								$(".sev_img3").slideDown("slow", 'easeOutBounce', function() {
									$(".sev_img4").slideDown("slow", 'easeOutBounce', function() {
										$(".sev_img5").slideDown("slow", 'easeOutBounce');
									});
								});
							});
						});
					}
				});
			}
			$(function() {
				//为导航绑订事件
				$(".navbar-nav li a").click(function() {
					//找到对应的id
					scTO($(this).attr("href"));
				});
				//关于我们滚动
				$(".about_content").scrollbox();
				//轮播滚动监听
				$('#myCarousel').on('slid.bs.carousel', function() {
					var html = $(this).find(".carousel-inner .active .carousel-caption").html();
					$(this).find(".banner_info").hide().html(html).fadeIn("slow");
				});
				//默认滚动到轮播
				scTO("#index");
			});
		</script>
		
	</head>

	<body data-spy="scroll" data-target="#navscroll" data-offset="100">
		<!--head-->
		<nav class="navbar navbar-default navbar-fixed-top yhead">
			<div class="container">
				<!-- Brand and toggle get grouped for better mobile display -->
				<div class="navbar-header">
					<button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#bs-example-navbar-collapse-1" style="margin-top: 42px;" aria-expanded="false">
				        <span class="sr-only">Toggle navigation</span>
				        <span class="icon-bar"></span>
				        <span class="icon-bar"></span>
				        <span class="icon-bar"></span>
				        <span class="icon-bar"></span>
				    </button>
					<a class="navbar-brand logo" href="index.html"><img src="img/logo.jpg" /></a>
				</div>
				<div class="collapse navbar-collapse nav_margin" id="bs-example-navbar-collapse-1">
					<ul class="nav navbar-nav">
						<li role="presentation"><a href="#index">首页</a></li>
						<li role="presentation"><a href="#about">关于巨藻</a></li>
						<li role="presentation"><a href="#service">核心服务</a></li>
						<li role="presentation"><a href="#bus">校企合作</a></li>
						<li role="presentation"><a href="#news">新闻资讯</a></li>
						<li role="presentation"><a href="#bottom">联系我们</a></li>
					</ul>
				</div>
			</div>
		</nav>  
		<!--end head-->

		<div style="height: 100px;" id="index"></div>
		<div class="ycontent bg-primary" style="position: relative;">
			<!--轮播start -->
			<div id="myCarousel" class="carousel slide" data-ride="carousel">
				<!-- Indicators -->
				<div class="banner_content">
					<div class="banner_info">
						<h3>巨藻创意科技</h3>
						<h3>锴国实业（上海）有限公司</h3>
						<br>
						<p>
							<a href="yuanku.html" target="_blank">查看项目 &gt;&gt;</a>
						</p>
					</div>

					<ol class="carousel-indicators">
						<li data-target="#myCarousel" data-slide-to="0" class="active"></li>
						<li data-target="#myCarousel" data-slide-to="1"></li>
						<li data-target="#myCarousel" data-slide-to="2"></li>
						<li data-target="#myCarousel" data-slide-to="3"></li>
						<li data-target="#myCarousel" data-slide-to="4"></li>
						<li data-target="#myCarousel" data-slide-to="5"></li>
					</ol>
				</div>

				<!-- Wrapper for slides -->
				<div class="carousel-inner" role="listbox">
					<div class="item active">
						<a href="yuanku.html"><img src="img/zbp2.jpg"></a>
						<div class="carousel-caption" style="display: none;">
							<h3>巨藻创意科技</h3>
							<h3>锴国实业（上海）有限公司</h3>
							<br>
							<p>
								<a href="yuanku.html">查看项目 &gt;&gt;</a>
							</p>
						</div>
					</div>
					<div class="item">
						<a href="fsd.html"><img src="img/zbp3.jpg"></a>
						<div class="carousel-caption" style="display: none;">
							<h3>商业互联网开发部</h3>
							<h3>项目开发案例展示</h3>
							<br>
							<p>
								<a href="fsd.html">查看项目 &gt;&gt;</a>
							</p>
						</div>
					</div>
					<div class="item">
						<a href="UI.html"><img src="img/zbp4.jpg"></a>
						<div class="carousel-caption" style="display: none;">
							<h3>商业视觉设计部</h3>
							<h3>与品牌策划服务</h3>
							<br>
							<p>
								<a href="UI.html">查看项目 &gt;&gt;</a>
							</p>
						</div>
					</div>
					<div class="item">
						<a href="yuanku_kjds.html"><img src="img/zbp5.jpg"></a>
						<div class="carousel-caption" style="display: none;">

							<h3>跨境电商</h3>
							<h3>与网络营销服务</h3>
							<br>
							<p>
								<a href="yuanku_kjds.html">查看项目 &gt;&gt;</a>
							</p>
						</div>
					</div>
					<div class="item">
						<a href="yk_zx.html"><img src="img/img_05.jpg"></a>
						<div class="carousel-caption" style="display: none;">
							<h3>储备精英 助学成才</h3>
							<h3>大学生就业与创业扶持计划</h3>
							<br>
							<p>
								<a href="yk_zx.html">查看项目 &gt;&gt;</a>
							</p>
						</div>
					</div>

					<div class="item">
						<a href="enterprise.html"><img src="img/img_04.jpg"></a>
						<div class="carousel-caption" style="display: none;">
							<h3>企业合作</h3>
							<h3>资源整合，互利共赢</h3>
							<br>
							<p>
								<a href="enterprise.html">查看项目 &gt;&gt;</a>
							</p>
						</div>
					</div>
				</div>
			</div>
			<!--轮播end -->
		</div>

		<div class="ycontent" id="about">
			<div class="container">
				<div class="row">
					<div class="col-md-7 col-xs-12 col-lg-6 about_img">
						<img src="img/zbp1.jpg" />
					</div>

					<div class="col-md-5 col-xs-12 col-lg-6 about_content">
						<ul>
							<li>
								<p>
									
									<a href="yuanku.html">泰州市康威医疗器械有限公司一家从事医疗器械、检验仪器和一次性耗材生产和销售的企业，公司拥有专业的生产、检测设备，主要产品有： 试管、吸管、吸头、移液器、离心管、培养皿、培养板、比色杯、样品杯、采样杯、盒子、架子、仪器、真空采血管、针等医用产品，我们秉承“诚信服务赢天下，品质信誉赢市场”的核心价值观，认为客户、供应商、公司员工等一切和自身有合作关系的单位和个人都是自己的合作伙伴，并只有通过努力为合作伙伴创造价值，才能体现自身的价值并获得发展和成功。</a>
								</p>
							</li>
							<li>
								<p>
									<a href="yuanku.html">展望未来，公司将以更加优质的产品和周到的服务，回馈予新老客户对我们的信任和支持，不断自我完善，以优质的产品和良好的服务，为人类的健康事业做出新的贡献！</a>
								</p>
							</li>
							<li>
								<p>
									<a href="yuanku.html">基于优质的校企合作资源，锴国实业公司同时为企业提供相关IT技术的内训服务，人才输送服务，高校IT人才实习实训服务以及大学生就业与创业扶持服务。通过整合人才和技术资源，锴国实业不断为广告和IT行业输送新鲜血液。</a>
								</p>
							</li>
							<li>
								<p>
									<a href="yuanku.html">锴国实业使命：为客户提供专业的，符合时代发展趋势并具有竞争力的品牌策划、IT技术及IT人才发展服务。</a>
								</p>
							</li>
							<li>
								<p>
									<a href="yuanku.html">锴国实业愿景：成为国内最权威的品牌策划、IT技术服务及高端人才培养方案的提供商。</a>
								</p>
							</li>
							<li>
								<p>
									<a href="yuanku.html">锴国实业核心价值观：专业、创新、服务、责任。</a>
								</p>
							</li>
							<li>
								<p>
									<a href="yuanku.html">锴国实业发展理念：鼓励源创意，追逐酷潮流。</a>
								</p>
							</li>
						</ul>
					</div>
				</div>
			</div>
		</div>

		<div class="ycontent bg-primary" id="service">
			<div class="container">
				<div class="row">
					<div class="col-xs-12 col-sm-3 col-md-2 sev_img1">
						<a href="subpage_visual.html"><img src="img/service_img_01.gif" /></a>
						<p>
							<a href="subpage_visual.html">商业视觉设计
							<br /> 与品牌策划服务</a>
						</p>
					</div>
					<div class="col-xs-12 col-sm-3 col-md-2 sev_img2">
						<a href="subpage_Inter.html"><img src="img/service_img_02.gif" /></a>
						<p>
							<a href="subpage_Inter.html">网站策划与
							<br/>互联网开发服务</a>
						</p>
					</div>
					<div class="col-xs-12 col-sm-3 col-md-2 sev_img3">
						<a href="yuanku_kjds.html"><img src="img/service_img_03.gif" /></a>
						<p>
							<a href="yuanku_kjds.html">跨境电商及
							<br/>网络营销服务</a>
						</p>
					</div>
					<div class="col-xs-12 col-sm-3 col-md-2 sev_img4">
						<a href="service_it.html"><img src="img/service_img_04.gif" /></a>
						<p>
							<a href="service_it.html">高端 IT人才
							<br/>培养与输送服务</a>
						</p>
					</div>
					<div class="col-xs-12 col-sm-3 col-md-2 sev_img5" style="margin-right: 0px;">
						<a href="yk_zx.html"><img src="img/service_img_05.gif" /></a>
						<p>
							<a href="yk_zx.html">储备精英 助学成才
							<br/>大学生就业与创业扶持</a>
						</p>
					</div>
				</div>
			</div>
		</div>

		<div class="ycontent" id="bus">
			<div class="container">
				<div class="row feature">
					<div class="col-md-7 col-xs-12 col-sm-12">
						<div class="row">
							<div class="col-md-4 col-xs-4" style="text-align: right;">
								<a href="enterprise.html"><img src="img/bus_img_02.gif" /></a>
							</div>
							<div class="col-md-8 col-xs-8">
								<dl>
									<dt>资源整合  互利共赢</dt>
									<dd><a href="enterprise.html">锴国实业创意自成立以来先后同电讯盈科，汇丰软件，中长康达，启宏科技，百度，前程无忧，广州欧蓝自动化公司，帅天广告公司，火之鸟广告公司，志科电子商务公司，腾科网络技术公司等华南区200多家公司建立了长期合作关系。其合作方式包括：企业品牌策划与广告设计服务；高端技术人才联合培养与输送合作...</a></dd>
								</dl>
							</div>
						</div>
						<div class="row">
							<div class="col-md-4 col-xs-4" style="text-align: right; margin-top: 20px;">
								<a href="school.html"><img src="img/bus_img_03.gif" /></a>
							</div>
							<div class="col-md-8 col-xs-8">
								<dl>
									<dt>优势互补，共享人才培养成果</dt>
									<dd><a href="school.html">自2010年以来，锴国实业依靠自身在业界良好的口碑和技术实力，先后同广东外语外贸大学，广美学院，五邑大学，广东工业大学，广州大学，广东轻工职业技术学院，广东工贸职业技术学院，广东农工商职业技术学院等30多家高校建立了平面广告设计，互联网特效设计，网站建设，软件开发，移动互联网开发等多个专业方向的实习实训合作...</a></dd>
								</dl>

							</div>
						</div>
					</div>
					<div class="col-md-5 col-xs-12 col-sm-12">
						<img class="feature-image img-responsive" src="img/bus_img_01.gif" alt="合作企业" style=" margin:0 auto;">
					</div>
				</div>
			</div>
		</div>
		<!--新闻资讯-->
		<!-- <div class="ycontent bg-primary" id="news">
			<div class="container">
				<div class="row">
					<div class="col-md-8 col-xs-12">
						<img src="img/news_img.gif" style="margin-top: 75px;width: 100%;" />
					</div>

					<div class="col-md-4 col-xs-12">
						<ul class="list-unstyled" style="margin-top: 100px;">
							<li><a href="yk_new.html">我与锴国实业有个约会@农工商计算机系校内周末...</a></li>
							<li><a href="http://www.yuanku.org/yuanku/mobile-third-113.html">圣诞？狂欢？~看锴国实业</a></li>
							<li><a href="http://www.yuanku.org/yuanku/mobile-third-107.html">主要看气质@松山职院第三批学员颜值爆表</a></li>
							<li><a href="http://www.yuanku.org/yuanku/mobile-third-108.html">白鹭时代进高校，北语IT精英论坛召开</a></li>
							<li><a href="http://www.yuanku.org/yuanku/mobile-third-106.html">锴国实业2016公益寒假@IT免费实训营招募啦！</a></li>
							<li><a href="http://www.yuanku.org/yuanku/mobile-third-101.html">2016年IT行业预测报告，五大发展趋势不容忽视</a></li>
							<li><a href="http://www.yuanku.org/yuanku/mobile-third-97.html">复合型IT人才培养探索-锴国实业@中元泰合作交流</a></li>
							<li><a href="http://www.yuanku.org/yuanku/mobile-third-53.html">2014年薪情大涨的12个科技职位</a></li>
							<li><a href="http://www.yuanku.org/yuanku/mobile-third-63.html">把时间分给靠谱的人和事</a></li>
							<li><a href="http://www.yuanku.org/yuanku/mobile-third-62.html">没有能不能，只有要不要</a></li>
							<li><a href="http://www.yuanku.org/yuanku/mobile-third-61.html">不值得定律 值得我们思考</a></li>
							<li><a href="http://www.yuanku.org/yuanku/mobile-third-54.html">做最好的自己，才能碰见最好的别人！</a></li>
						</ul>
					</div>
				</div>
			</div>
		</div> -->

		<!--底部联系我们-->
		<div class="bg-primary" id="bottom">
			<div class="container-fluid">
				<div class="row" style="margin-top: 100px;">
					<img src="img/botton_img.jpg" style="width: 100%;" />
				</div>
			</div>

			<div class="container">
				<div class="row">
					<div class="col-md-5">
						<img src="img/addr_img.gif" />
					</div>
					<div class="col-md-2">
						<img src="img/erweima.png" />
						<p>扫一扫 加关注</p>
					</div>
					<div class="col-md-4">
						<h2>锴国实业（上海）有限公司</h2>
						<address>
							公司地址：上海市闵行区莲花南路3999弄6号楼225-231<br />
							
							<abbr style="margin-right: 20px;">电话：021-33269651</abbr>
							
						</address>
					</div>
				</div>
			</div>
		</div>
		<div style="height: 100px;"></div>
		<script>
		var _hmt = _hmt || [];
		(function() {
		  var hm = document.createElement("script");
		  hm.src = "//hm.baidu.com/hm.js?ba91ab6d2e13683d11c231b771efe2dd";
		  var s = document.getElementsByTagName("script")[0];
		  s.parentNode.insertBefore(hm, s);
		})();
		</script>
	</body>

</html>
