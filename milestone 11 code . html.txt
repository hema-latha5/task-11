<html>
<body>
<center>
<h1><u>Regular Expressions</u></h1>
</center>
<h2>EMAIL VERIFICATION</h2>
<h2>pattern that matches e-mail addresses</h2>
        <script>
        function valid_email(str)
{
var mailformat = /^\w+([\.-]?\w+)@\w+([\.-]?\w+)(\.\w{2,3})+$/;  
if(mailformat.test(str))
{  
document.write("Valid email address!");  
}  
else  
{  
document.write("You have entered an invalid email address!");  
}
}

valid_email('me-info@example.com');
        </script>
    </body>
<body>
<center>
<h1><u>JavaScript Objects</u></h2>
</center>


<p id="demo"></p>

<script>
// Initialize an object
const car = {
     type:'volvo',
    color: 'Red',
    number: 5   
};

// Initialize another object
const somemore = {
    vechicle:'car',
    fruit: 'Mango',
    movies: ["Spider Man", "Conjuring"],   
};

// Merge the objects
document.write("assign() method :"+"    ");
document.write(Object.assign(car, somemore));
document.write("<br>"+"isFrozen() method  :"+" ");
document.write(Object.isFrozen(car));

function vechicles() {
    this.name = 'bike';
}
function bullet() {
    vechicles.call(this);
}
bullet.prototype = Object.create(vechicles.prototype);
const app = new bullet();
document.write("<br>"+"create() method  :"+" ");
document.write(app.name);
const obj=Object.seal(car);
obj.color='black';
document.write("<br>"+"seal() method  :"+" ");
document.write(obj.color);
document.write("<br>"+"isSealed() method  :"+" ");
document.write(Object.isSealed(car));
</script>
</body>

<body>
<center>
<h1><u>Prototype based Object Oriented Programming</u></h1>
</center>
<p id="demo"></p>
<script>
const o = {
  a: 1,
  b: 2,
  proto: {
    c: 3,
  },
};

document.write(o.a); // 1
document.write("<br>");
document.write(o.b); // 2
document.write("<br>");
document.write(o.c); // 3
document.write("<br>");
</script>
</body>

<body>
<center>
<h1><u>Classes</u></h1>
</center>
<h2>Pen constructor function that has name, color, and price properties. Use new keyword with the Pen constructor to create an object pen1. Add a new function to the Pen constructor. To do this we need to add the function into the prototype property of Pen. showPrice method should be called and execute the showprice method</h2>
<script>
function Pen(name, color, price) {
    this.name = name;
    this.color = color;
    this.price = price;
}
const pen1 = new Pen("Marker", "Blue", "$3");
Pen.prototype.showPrice = function(){
    document.write(`Price of ${this.name} is ${this.price}`);
}
pen1.showPrice();
</script>
</body>

<body>
<center>
<h1><u>Meta Programming and using the Proxy concept</u></h1>
</center>
<script>
let handler = {
  get(target, name) {
    return name in target ? target[name] : "usha"
  }
}

let p = new Proxy({}, handler)
p.a = 1
document.write(p.a+"<br>"+ p.b);
</script>
</body>
</html>