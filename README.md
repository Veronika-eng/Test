"use strict"
/*1. Задача. Напишите скрипт, который считает количество секунд в часе.*/
alert('Количество секунд в часе: '+ 60*60);

/*2. Задача. Дан массив с элементами 'Привет, ', 'мир' и '!'. Необходимо записать в
переменную text фразу 'Привет, мир!', а затем вывести на экран содержимое этой
переменной.*/
let elements=['Привет,','мир','!'];
let str=elements.join (' ');
alert (str);

/*3. Задача. В переменной min лежит число от 0 до 59. Определите в какую четверть
часа попадает это число (в первую, вторую, третью или четвертую).*/
let min = prompt ('Введите количество минут');
if (min <= 15) {
  alert ('Первая четверть часа');
}
else if (min <= 30) {
  alert ('Вторая четверть часа');
}
else if (min <= 45) {
  alert ('Третья четверть часа');
}
else if (min <= 59) {
  alert ('Четвертая четверть часа');
}

/*4. Задача. Дан массив с элементами [1, 2, 3, 4, 5]. С помощью цикла for выведите все эти
элементы на экран*/
let arr=[1,2,3,4,5];
let str=' ';
for (let i=0;i<arr.length;i++) {
  str=str+arr[i]+' ';
}
alert(str);

/*5. Задача. Даны переменные a и b. Проверьте, что a делится без остатка на b. Если это
так - выведите 'Делится' и результат деления, иначе выведите 'Делится с остатком' и
остаток от деления.*/
let a=prompt('Введите число a: ');
let b=prompt('Введите число b: ');

if(a%b==0) {
let div=a/b; 
alert('Делится: ' +div);
}
else {
let notdiv=a%b;
alert('Делится с остатком: ' +notdiv);
}

/*6. Задача. Дана строка 'aaa bbb ccc'. Вырежите из нее слово 'bbb' тремя разными способами
(через substr, substring, slice).*/
let str='aaa bbb ccc';
//Метод substr
alert('Метод substr : '+str.substr(0,4)+str.substr(-4,4));
//Метод substring
alert('Метод substring : '+str.substring(0,4)+str.substring(7,11));
//Метод slice
alert('Метод slice : '+str.slice(0,4)+str.slice(7));

/*7. Задача. Дан массив ['a', 'b', 'c']. Добавьте ему в конец элементы 1, 2, 3.*/
let arr1=['a','b','c'];
let arr2=[1,2,3];
let newArr=arr1.concat (arr2);
alert(newArr);

/*8. Задача. Дана строка, например, '123456'. Переверните эту строку (сделайте из нее '654321')не используя цикл*/
let str='123456';
str=str.split('');
str.reverse();
let str1=str.join('');
alert(str1);

/*9. Задача. Сделайте функцию, которая возвращает квадрат числа. Число передается
параметром.*/
let userNum=prompt ('Введите число');
function calc (a) {
  let b=a*a;
  return b;
}
alert('Квадрат введённого числа равен : ' +calc(userNum));

/*10. Задача. Дано число, например 31. Проверьте, что это число не делится ни на одно другое
число кроме себя самого и единицы. То есть в нашем случае нужно проверить, что число 31
не делится на все числа от 2 до 30. Если число не делится - выведите 'false', а если делится -
выведите 'true'.*/
let number=prompt('Введите число: ');
let delitsya=0;

for (let i=2; i<number; i++) {
  if(number%i==0) {
  delitsya=1;
  break;
  }
  else {
  delitsya=0;
  }
}
if(delitsya==1) {
  alert('True');
{
else {
  alert ('False');
}

/*11. Задача. Сделайте функцию, которая параметрами принимает 2 числа. Если их сумма больше
10 - пусть функция вернет true, а если нет - false*/
let a=prompt('Введите число a');
let b=prompt('Введите число b');
alert (CheckSum (a,b)); 
function CheckSum (a,b) {
  if ((+a + +b) > 10) {
  return true;
  }
  else {        
  return false;
  }
}

/*12. Задача. С помощью цикла for сформируйте строку '987654321' и запишите ее в
переменную str.*/
let str='';
for(let i=9; i>0; i--) {
str=str+i;    
alert(str);
}

/*13. Задача. Заполните массив следующим образом: в первый элемент запишите '1', во второй
'22', в третий '333' и так далее.*/
let arr=[];
for (let i=1; i<10; i++) {
let str='';
for (let j=1; j<=i; j++) {
str=str + i;
}
arr.push(str);
}
alert(arr);

/*14. Задача. Сделайте функцию isNumberInRange, которая параметром принимает число и
проверяет, что оно больше нуля и меньше 10. Если это так - пусть функция возвращает true,
если не так - false.*/
let a=prompt('Введите число');

if (isNumberInRange (a)) {
  alert ('True');
}
else {
  alert ('False');
}

function isNumberInRange (a) {
  if (a > 0 && a < 10) {
  return true;
  }
  else {
  return false;
  }
}

/*15. Задача. Дана строка вида 'var_text_hello'. Сделайте из него текст 'varTextHello'.*/
let str='var_text_hello';
str=str.slice(0,3)+str.slice(4,8)+str.slice(9);
str=str.split('');
for(let i=0;i<=11;i++){
  if(i==3 || i==7){
  str[i]=str[i].toUpperCase();
  }
  else{
  str[i]=str[i];
  }
}
alert(str.join(''));

/*16. Задача. Дано число. Сложите его цифры. Если сумма получилась более 9-ти, опять сложите
его цифры. И так, пока сумма не станет однозначным числом (9 и менее)*/
let arr=prompt('Введите число');
DigSum(arr);

function DigSum(dig) {
let sum=0;
dig=dig.split('');
for(let i=0;i<dig.length;i++){
  sum=sum+dig[i];
}
if(sum>9) {
  DigSum(sum+ '');
}
else{
  alert(sum);
}
}

/*17. Задача. Выведите с помощью цикла столбец чисел от 100 до 1.*/
let str=' ';
for (let i=100; i>=1; i--) {
  str = str + i + '\n';
}
console.log (str);

/*18. Задача. Выведите на экран текущий месяц словом, по-русски.*/
let months=['Январь','Февраь','Март','Апрель','Май','Июнь','Июль','Август','Сентябрь','Октябрь','Ноябрь','Декабрь'];
let date=new Date();
let month=date.getMonth();
alert(months[month]);

/*20. Задача. Дана кнопка. По нажатию на эту кнопку прокрутите окно браузера до самого низа*/
let button=document.getElementById('button');
button.addEventListener('click', function() {
let elem=document.getElementById('elem');
elem.scrollTop=elem.scrollHeight;
})

/*21. Задача. Дан див. Внутри него вначале находится просто текст, а затем span:
<div> text <span>span</span></div> Выведите на экран находящийся в начале дива текст.*/
let text=document.body.firstElementChild('text');
console.log(text);
