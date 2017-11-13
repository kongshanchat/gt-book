$(function() {
	FastClick.attach(document.body);

});

function cal() {
	var total = 12;
	var num = 2;
	var cell_num = 8;
	var html = "";
	for(var i = 1; i <= num; i++) {
		var max = i * cell_num;
		html += '<div class="swiper-slide"><div class="sort-box"><ul>';
		for(j = 1; j <= total; j++) {
			if(j <= max - (i - 1) * total) {
				html += '<li><img src="img/money.png"><span class="sort-icon-title">化工</span></li>';
			}
		}

		html += "</ul></div></div>";
	}
	$('.swiper-icon .swiper-wrapper').append(html)

}
cal();

var swiper = new Swiper('.swiper-icon', {
	pagination: '.swiper-pagination',
	paginationClickable: true
});


	$(function() {
		FastClick.attach(document.body);

	});

function cal() {
	var total = 12;
	var num = 2;
	var cell_num = 8;
	var html = "";
	for(var i = 1; i <= num; i++) {
		var max = i * cell_num;
		html += '<div class="swiper-slide"><div class="sort-box"><ul>';
		for(j = 1; j <= total; j++) {
			if(j <= max - (i - 1) * total) {
				html += '<li><img src="img/money.png"><span class="sort-icon-title">化工</span></li>';
			}
		}

		html += "</ul></div></div>";
	}
	$('.swiper-icon .swiper-wrapper').append(html)

}
cal();

var swiper = new Swiper('.swiper-icon', {
	pagination: '.swiper-pagination',
	paginationClickable: true
});





	var pages = 1;
var sb = 1;
var loading = false;

$(document.body).infinite().on("infinite", function() {
	if(loading) return;
	loading = true;
	sb++;
	if($('.weui-loadmore').attr('has-more') == 0) {
		return false;
	}

	$.ajax({
		crossOrigin: true,
		async: false,
		type: 'GET',
		url: 'https://app.hg707.com/index.php?s=/Api2/book/search&hot=1&page=' + sb,
		dataType: 'json',
		success: function(e) {
			var html = "";
			if(e.data.length == 0) {
				$('.weui-loadmore__tips').text('已经到底了哟！')
				$('.weui-loading').hide();
				$('.weui-loadmore').attr('has-more', 0);
				return false;
			}

			$.each(e.data, function(a, b) {
				html += '<li><a href="#">';
				html += '<div class="bookface">';
				html += '<img class="lazy" data-original="' + b.cover[0].img_url + '">';
				html += '</div>';
				html += '<div class="book-text">';
				html += '<h3>' + b.name + '</h3>';
				html += '<p class="book-info">' + b.summary + '</p>';
				html += '<p class="book-price"><img src="img/money.png"> <span>' + b.price + '</span></p>';
				html += '</div>';
				html += '</a>';
				html += '</li>';
			})

			loading = false;
			$(html).insertBefore('.weui-loadmore');
			$("img.lazy").lazyload({
				placeholder: "img/chou.png",
				threshold: 200,
				event: 'scroll',
				//failurelimit : 10 ,
				effect: "fadeIn"
			});

		}
	})

});

$(function() {
		$.ajax({
			crossOrigin: true,
			async: false,
			type: 'GET',
			url: 'https://app.hg707.com/index.php?s=/Api2/book/banner&',
			dataType: 'json',
			success: function(data) {
				var html = "";
				$.each(data.data, function(a, b) {
					html += '<div class="swiper-slide"><img src="' + b.cover[0].img_url + '"/></div>';
				})

				$('.lunbo .swiper-wrapper').append(html)
			}
		})

		$(".swiper-container").swiper({
			loop: true,
			autoplay: 3000
		});

		$.ajax({
			crossOrigin: true,
			async: false,
			type: 'GET',
			url: 'https://app.hg707.com/index.php?s=/Api2/book/search&hot=1&page=1',
			dataType: 'json',
			success: function(e) {
				//console.log(e.data)
				var html = "";

				$.each(e.data, function(a, b) {

					html += '<li><a href="#">';
					html += '<div class="bookface">';
					html += '<img class="lazy" data-original="' + b.cover[0].img_url + '">';
					html += '</div>';
					html += '<div class="book-text">';
					html += '<h3>' + b.name + '</h3>';
					html += '<p class="book-info">' + b.summary + '</p>';
					html += '<p class="book-price"><img src="img/money.png"> <span>' + b.price + '</span></p>';
					html += '</div>';
					html += '</a>';
					html += '</li>';
				})

				$(html).insertBefore('.weui-loadmore');
			}
		})

		$("img.lazy").lazyload({
			placeholder: "img/chou.png",
			threshold: 200,
			event: 'scroll',
			//failurelimit : 10 ,
			effect: "fadeIn"
		});

	}) 