// 阅读推荐的链接，复习JavaScript中数组的相关方法

// 写程序判断下列变量是不是数组类型。
var a = '[a, b, c, d]';
var b = [1, 2, 3, 4];
console.log(typeof a);
console.log(typeof b);


// 编写程序，将下面数组中的每一项都乘以2。
var a = [1, 2, 3, 4, 5];
for (var i = 0; i < 5; i++) {
    a[i] = a[i]*2;
}
console.log(a);


// 编写程序，按下面的要求输出结果。
var colors = ["Red", "Green", "White", "Black"];
//TODO case 1 output: 'Red Green White Black'
var str = "";
for (var i = 0; i < colors.length; i++) {
    str += colors[i]
    if (i != colors.length - 1) {
        str += " ";
    }
}
console.log(str);

// case 2 output: 'Red+Green+White+Black'
var str = "";
for (var i = 0; i < colors.length; i++) {
    str += colors[i]
    if (i != colors.length - 1) {
        str += "+";
    }
}
console.log(str);

// case 3 output: 'Red,Green,White,Black'
var str = "";
for (var i = 0; i < colors.length; i++) {
    str += colors[i]
    if (i != colors.length - 1) {
        str += ",";
    }
}
console.log(str);
// 编写程序，将下面数组中的数字按从大到小的顺序排序。
var a = [5, 1, 8, 10, 4];
//TODO should output: [10,8,5,4,1]
var temp;
for (var i = 0; i < a.length - 1; i++) {
    for (var j = a.length - 1; j > i; j--) {
        if (a[j - 1] < a[j]) {
            temp = a[j - 1];
            a[j - 1] = a[j];
            a[j] = temp;
        }
    }
}
console.log(a)

// 编程程序，找出下列数组中出现频率最高的元素。
var a = [3, 'a', 'a', 'a', 2, 3, 'a', 3, 'a', 2, 4, 9, 3];
//TODO should output: 'a'
var a = [3, 'a', 'a', 'a', 2, 3, 'a', 3, 'a', 2, 4, 9, 3];
function findMost2(a) {
    var h = {};
    var maxNum = 0;
    var maxEle = null;
    for (var i = 0; i < a.length; i++) {
        var b = a[i];
        h[b] === undefined ? h[b] = 1 : (h[b]++);
        if (h[b] > maxNum) {
            maxEle = b;
            maxNum = h[b];
        }
    }
    return maxEle ;
}
console.log(findMost2(a));
