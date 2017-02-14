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
// var li = $('<li>', {"class": "bio-info-item"}, 'Last Updated: ', Date());
// $('.bio-info').append(li);

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
// $(leftSpan).addClass('bio-info-item');
// $(rightSpan).addClass('bio-info-item');
$(listItem).appendTo('.bio-info');

Stretch Exercise
All in Vanilla Js Now:
1.
document.getElementsByTagName('img')[0].setAttribute('src', 'http://placebear.com/400/300');
document.getElementById('left-image').getElementsByTagName('img')[0].setAttribute('src', 'http://placebear.com/400/300');
2.
document.getElementsByTagName('h1')[0].innerText = 'Joey';
3.
document.getElementById('employment').getElementsByClassName('info-title')[0].innerText = 'Hello';
4.
document.getElementById('time-travel').parentElement.remove();
5.
document.body.style.backgroundColor = 'red';
6.
var x = document.getElementsByClassName('highlight')
for (var step = 0; step < x.length; step++) {
  document.getElementsByClassName('highlight')[step].style.color = 'grey';
}
7.
document.getElementsByTagName('h1')[0].style.fontFamily = 'monospace';
8.
var x = document.getElementsByClassName('action-icon-bg');
for (var step = 0; step < x.length; step++) {
  document.getElementsByClassName('action-icon-bg')[step].addEventListener('click', function() { this.style.backgroundColor = 'red'; });
}
9.
document.getElementById('name').setAttribute('placeholder', 'identify yourself');
10.
document.getElementById('message').setAttribute('placeholder', 'state your business');
11.
document.getElementById('name').setAttribute('value', 'your nemesis')
12.
document.getElementById('email').setAttribute('value', 'koalathebear@gmail.com');
13.
document.getElementById('submit').setAttribute('value', 'En garde!');
Bonus
1.
document.getElementById('submit').setAttribute('disabled', 'true');
2.
document.getElementsByTagName('ul')[0].remove('bio-info');
Adding elements to the DOM
1.
var x = document.getElementById('right-image').getElementsByTagName('img')[0].cloneNode();
document.getElementsByTagName('section')[0].appendChild(x);
2.
for (var step = 0; step < 10; step++) {
  var x = document.getElementById('right-image').getElementsByTagName('img')[0].cloneNode();
  document.getElementsByTagName('section')[0].appendChild(x);
}
