<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>حاسبة معدل الفصل الدراسي</title>
    <!-- Google Font: Cairo -->
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Cairo', sans-serif; /* Apply Cairo font */
            background-color: #121212; /* Dark background color */
            color: #e0e0e0; /* Light text color */
            margin: 0;
            padding: 20px;
            text-align: center;
        }
        .container {
            max-width: 700px;
            margin: 0 auto;
            background: #1e1e1e; /* Dark container background */
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(255, 255, 255, 0.1);
        }
        h1 {
            color: #f4f4f4;
            margin-bottom: 20px;
        }
        .subject {
            border: 1px solid #333;
            padding: 10px;
            margin-bottom: 10px;
            border-radius: 5px;
            text-align: center; /* Align subject names in the center */
            background-color: #2c2c2c; /* Dark background for subjects */
        }
        .subject h2 {
            margin: 0;
            font-size: 16px;
            margin-bottom: 10px;
            color: #fff;
        }
        table {
            width: 100%;
            margin-bottom: 10px;
            border-collapse: collapse;
            direction: rtl; /* Right to left */
        }
        table td, table th {
            border: 1px solid #444;
            padding: 8px;
            text-align: center;
            background-color: #333; /* Dark background for table cells */
        }
        input[type="text"], input[type="number"] {
            width: 50%; /* Reduced width of coefficient input */
            padding: 8px;
            border: 1px solid #555;
            border-radius: 5px;
            background-color: #444;
            color: #fff;
        }
        button {
            background-color: #007BFF;
            color: #fff;
            border: none;
            padding: 10px 20px;
            font-size: 16px;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 10px;
        }
        button:hover {
            background-color: #0056b3;
        }
        .result {
            margin-top: 20px;
            font-size: 18px;
            color: #28a745;
        }
        .error {
            color: #dc3545;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>حاسبة معدل الفصل الدراسي</h1>
        <div id="subjects-container">
            <!-- الرياضيات -->
            <div class="subject" data-coefficient="7">
                <h2>الرياضيات <label>(المعامل: <input type="number" value="7" class="coefficient-input">)</label></h2>
                <table>
                    <tr>
                        <th>الاختبار 1</th>
                        <th>الاختبار 2</th>
                        <th>الاختبار 3</th>
                        <th>الاختبار 4</th>
                        <th>الاختبار 5</th>
                    </tr>
                    <tr>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                    </tr>
                </table>
            </div>

            <!-- الفيزياء -->
            <div class="subject" data-coefficient="7">
                <h2>الفيزياء <label>(المعامل: <input type="number" value="7" class="coefficient-input">)</label></h2>
                <table>
                    <tr>
                        <th>الاختبار 1</th>
                        <th>الاختبار 2</th>
                        <th>الاختبار 3</th>
                        <th>الاختبار 4</th>
                        <th>الاختبار 5</th>
                    </tr>
                    <tr>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                    </tr>
                </table>
            </div>

            <!-- علوم الحياة والارض -->
            <div class="subject" data-coefficient="5">
                <h2>علوم الحياة والارض <label>(المعامل: <input type="number" value="5" class="coefficient-input">)</label></h2>
                <table>
                    <tr>
                        <th>الاختبار 1</th>
                        <th>الاختبار 2</th>
                        <th>الاختبار 3</th>
                        <th>الاختبار 4</th>
                        <th>الاختبار 5</th>
                    </tr>
                    <tr>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                    </tr>
                </table>
            </div>

            <!-- الفرنسية -->
            <div class="subject" data-coefficient="4">
                <h2>الفرنسية <label>(المعامل: <input type="number" value="4" class="coefficient-input">)</label></h2>
                <table>
                    <tr>
                        <th>الاختبار 1</th>
                        <th>الاختبار 2</th>
                        <th>الاختبار 3</th>
                        <th>الاختبار 4</th>
                        <th>الاختبار 5</th>
                    </tr>
                    <tr>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                    </tr>
                </table>
            </div>

            <!-- الرياضة -->
            <div class="subject" data-coefficient="4">
                <h2>الرياضة <label>(المعامل: <input type="number" value="4" class="coefficient-input">)</label></h2>
                <table>
                    <tr>
                        <th>الاختبار 1</th>
                        <th>الاختبار 2</th>
                        <th>الاختبار 3</th>
                        <th>الاختبار 4</th>
                        <th>الاختبار 5</th>
                    </tr>
                    <tr>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                    </tr>
                </table>
            </div>

            <!-- الفلسفة -->
            <div class="subject" data-coefficient="2">
                <h2>الفلسفة <label>(المعامل: <input type="number" value="2" class="coefficient-input">)</label></h2>
                <table>
                    <tr>
                        <th>الاختبار 1</th>
                        <th>الاختبار 2</th>
                        <th>الاختبار 3</th>
                        <th>الاختبار 4</th>
                        <th>الاختبار 5</th>
                    </tr>
                    <tr>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                    </tr>
                </table>
            </div>

            <!-- الانجليزية -->
            <div class="subject" data-coefficient="2">
                <h2>الانجليزية <label>(المعامل: <input type="number" value="2" class="coefficient-input">)</label></h2>
                <table>
                    <tr>
                        <th>الاختبار 1</th>
                        <th>الاختبار 2</th>
                        <th>الاختبار 3</th>
                        <th>الاختبار 4</th>
                        <th>الاختبار 5</th>
                    </tr>
                    <tr>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                    </tr>
                </table>
            </div>

            <!-- التربية الاسلامية -->
            <div class="subject" data-coefficient="2">
                <h2>التربية الاسلامية <label>(المعامل: <input type="number" value="2" class="coefficient-input">)</label></h2>
                <table>
                    <tr>
                        <th>الاختبار 1</th>
                        <th>الاختبار 2</th>
                        <th>الاختبار 3</th>
                        <th>الاختبار 4</th>
                        <th>الاختبار 5</th>
                    </tr>
                    <tr>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                    </tr>
                </table>
            </div>

            <!-- العربية (New) -->
            <div class="subject" data-coefficient="2">
                <h2>العربية <label>(المعامل: <input type="number" value="2" class="coefficient-input">)</label></h2>
                <table>
                    <tr>
                        <th>الاختبار 1</th>
                        <th>الاختبار 2</th>
                        <th>الاختبار 3</th>
                        <th>الاختبار 4</th>
                        <th>الاختبار 5</th>
                    </tr>
                    <tr>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                    </tr>
                </table>
            </div>

            <!-- السلوك (New) -->
            <div class="subject" data-coefficient="1">
                <h2>السلوك <label>(المعامل: <input type="number" value="1" class="coefficient-input">)</label></h2>
                <table>
                    <tr>
                        <th>الاختبار 1</th>
                        <th>الاختبار 2</th>
                        <th>الاختبار 3</th>
                        <th>الاختبار 4</th>
                        <th>الاختبار 5</th>
                    </tr>
                    <tr>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                        <td><input type="text" class="quiz" placeholder="الدرجة"></td>
                    </tr>
                </table>
            </div>

        </div>
        <button onclick="calculateSemesterAverage()">حساب معدل الفصل الدراسي</button>
        <div id="result" class="result"></div>
    </div>

<script>
    function calculateSemesterAverage() {
        const subjects = document.querySelectorAll('.subject');
        const resultDiv = document.getElementById('result');

        let totalWeighted = 0;
        let totalCoefficients = 0;

        try {
            subjects.forEach(subject => {
                const coefficientInput = subject.querySelector('.coefficient-input');
                const quizzes = subject.querySelectorAll('.quiz');
                const grades = Array.from(quizzes).map(input => parseFloat(input.value.trim()));
                let coefficient = parseFloat(coefficientInput.value);

                if (grades.every(grade => !isNaN(grade))) {
                    const averageGrade = grades.reduce((sum, grade) => sum + grade, 0) / grades.length;
                    totalWeighted += averageGrade * coefficient;
                    totalCoefficients += coefficient;
                }
            });

            if (totalCoefficients > 0) {
                const semesterAverage = totalWeighted / totalCoefficients;
                resultDiv.textContent = `معدل الفصل الدراسي الخاص بك هو: ${semesterAverage.toFixed(2)}`;
                resultDiv.classList.remove('error');
                resultDiv.classList.add('success');
            } else {
                resultDiv.textContent = "يرجى إدخال الدرجات.";
                resultDiv.classList.add('error');
                resultDiv.classList.remove('success');
            }
        } catch (error) {
            resultDiv.textContent = "حدث خطأ في حساب معدل الفصل الدراسي. يرجى التحقق من مدخلاتك.";
            resultDiv.classList.add('error');
        }
    }
</script>

<footer style="margin-top: 20px; color: #f4f4f4; font-size: 14px;">
    <p>by Abdellah Riyaf</p>
</footer>

</body>
</html>
