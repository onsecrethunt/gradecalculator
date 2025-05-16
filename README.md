# gradecalculator
How GradeCalculator.college Works

---

### 3. README.md for **gradecalculator.college**

```markdown
# GradeCalculator.college

An easy-to-use grade calculator that computes weighted grades for students.

## How it works

Takes score and weight input, calculates weighted score using JavaScript.

### Demo snippet

```html
<input id="score" type="number" placeholder="Score" />
<input id="weight" type="number" placeholder="Weight (%)" />
<button onclick="calculateGrade()">Calculate</button>
<div id="result"></div>

<script>
function calculateGrade() {
  const score = parseFloat(document.getElementById('score').value);
  const weight = parseFloat(document.getElementById('weight').value);
  if(isNaN(score) || isNaN(weight)) {
    alert('Please enter valid numbers');
    return;
  }
  const weighted = (score * weight) / 100;
  document.getElementById('result').textContent = 'Weighted Score: ' + weighted.toFixed(2);
}
</script>
