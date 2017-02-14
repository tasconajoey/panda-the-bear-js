1.
$('img.profile-image').attr('src', 'http://placebear.com/400/300');
$('#left-image img').attr('src', 'http://placebear.com/400/300');
2.
$('h1.highlight').text('Joey');
3.
$('#employment .info-title').text('Hello');
4.
$('#time-travel').parent().remove();
5.
$('body').css('background-color', 'red');
6.
$('.highlight').css('color', 'grey');
7.
$('h1').css('font-family', 'monospace');
8.
$('.action-icon-bg').click(function() { $(this).css('background-color', 'blue'); });
9.
$('#name').attr('placeholder', 'identify yourself');
10.
$('#message').attr('placeholder', 'state your business');
11.
$('#name').attr('value', 'your nemesis');
12.
$('#email').attr('value', "koalathebear@gmail.com");
13.
$('#submit').attr('value', 'En garde!');
Bonus
1.
$('#submit').attr('disabled', 'true');
2.
$('.bio-info').empty();
Adding elements to the DOM
1.
$('#right-image img').clone().insertAfter('section').css({'text-align': 'center', 'margin': 'auto','border': '20px solid red', 'float': 'right', 'width': '65%'});
2.
for (var step = 0; step < 10; step++) {
  $('#right-image img').clone().insertAfter('section').css({'text-align': 'center', 'margin': 'auto','border': '20px solid red', 'float': 'right', 'width': '65%'});
}
3.
<!-- var li = $('<li>', {"class": "bio-info-item"}, 'Last Updated: ', Date());
$('.bio-info').append(li); -->

var listItem = document.createElement('li');
var leftSpan = document.createElement('span');
var rightSpan = document.createElement('span');
var lastUpdated = document.createTextNode('Page last updated on');
var lastUpdatedDate = document.createTextNode(Date());

leftSpan.appendChild(lastUpdated);
listItem.appendChild(leftSpan);
rightSpan.appendChild(lastUpdatedDate);
listItem.appendChild(rightSpan);
$(listItem).addClass('bio-info-item');
$(leftSpan).addClass('bio-info-item');
$(rightSpan).addClass('bio-info-item');
$(listItem).appendTo('.bio-info');
