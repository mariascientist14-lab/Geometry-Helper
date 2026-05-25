<script>

function calculateTriangle() {

    let h = parseFloat(document.getElementById("triHeight").value);
    let b = parseFloat(document.getElementById("triBase").value);
    let s1 = parseFloat(document.getElementById("triSide1").value);
    let s2 = parseFloat(document.getElementById("triSide2").value);

    if (isNaN(h) || isNaN(b) || isNaN(s1) || isNaN(s2)) {
        document.getElementById("triOutput").innerText =
        "Please enter valid numbers.";
        return;
    }

    let area = (b * h) / 2;
    let perimeter = b + s1 + s2;

    document.getElementById("triOutput").innerText =
`TRIANGLE STEP BY STEP

Step 1:
Area Formula = (base × height) ÷ 2

Step 2:
(${b} × ${h}) ÷ 2

Step 3:
${b * h} ÷ 2 = ${area}

-------------------

Perimeter Formula:
base + side1 + side2

${b} + ${s1} + ${s2} = ${perimeter}`;
}

function calculateCircle() {

    let r = parseFloat(document.getElementById("circRadius").value);

    if (isNaN(r)) {
        document.getElementById("circOutput").innerText =
        "Please enter a valid number.";
        return;
    }

    let area = Math.PI * r * r;
    let circumference = 2 * Math.PI * r;

    document.getElementById("circOutput").innerText =
`CIRCLE STEP BY STEP

Area Formula:
π × r²

π × ${r} × ${r}

Area = ${area.toFixed(2)}

-------------------

Circumference Formula:
2 × π × r

2 × π × ${r}

Circumference = ${circumference.toFixed(2)}`;
}

function calculateRectangle() {

    let l = parseFloat(document.getElementById("rectLength").value);
    let w = parseFloat(document.getElementById("rectWidth").value);

    if (isNaN(l) || isNaN(w)) {
        document.getElementById("rectOutput").innerText =
        "Please enter valid numbers.";
        return;
    }

    let area = l * w;
    let perimeter = 2 * (l + w);

    document.getElementById("rectOutput").innerText =
`RECTANGLE STEP BY STEP

Area Formula:
length × width

${l} × ${w} = ${area}

-------------------

Perimeter Formula:
2(length + width)

2(${l} + ${w})

2(${l + w}) = ${perimeter}`;
}

function calculateTrapezoid() {

    let t = parseFloat(document.getElementById("trapTop").value);
    let b = parseFloat(document.getElementById("trapBottom").value);
    let h = parseFloat(document.getElementById("trapHeight").value);
    let l = parseFloat(document.getElementById("trapLeft").value);
    let r = parseFloat(document.getElementById("trapRight").value);

    if (isNaN(t) || isNaN(b) || isNaN(h) || isNaN(l) || isNaN(r)) {
        document.getElementById("trapOutput").innerText =
        "Please enter valid numbers.";
        return;
    }

    let area = ((t + b) * h) / 2;
    let perimeter = t + b + l + r;

    document.getElementById("trapOutput").innerText =
`TRAPEZOID STEP BY STEP

Area Formula:
((top + bottom) × height) ÷ 2

((${t} + ${b}) × ${h}) ÷ 2

(${t + b} × ${h}) ÷ 2

${(t + b) * h} ÷ 2 = ${area}

-------------------

Perimeter Formula:
top + bottom + left + right

${t} + ${b} + ${l} + ${r} = ${perimeter}`;
}

function checkQuiz() {

    let score = 0;

    let q1 = parseFloat(document.getElementById("q1").value);
    let q2 = parseFloat(document.getElementById("q2").value);
    let q3 = parseFloat(document.getElementById("q3").value);

    let result = "";

    if (q1 === 20) {
        score++;
        result += "Question 1: Correct!\n";
    } else {
        result += "Question 1: Wrong. 5 × 4 = 20\n";
    }

    if (q2 === 9) {
        score++;
        result += "Question 2: Correct!\n";
    } else {
        result += "Question 2: Wrong. (6 × 3) ÷ 2 = 9\n";
    }

    if (q3 === 12) {
        score++;
        result += "Question 3: Correct!\n";
    } else {
        result += "Question 3: Wrong. 3 + 4 + 5 = 12\n";
    }

    result += `\nFinal Score: ${score}/3`;

    document.getElementById("quizOutput").innerText = result;
}

</script>
