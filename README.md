<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NetZeroNow | Textile Industry Carbon Awareness</title>
    
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600&family=Playfair+Display:ital,wght@0,600;0,700;1,400&display=swap" rel="stylesheet">

    <style>
        /* Base Reset & Variables */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary-green: #234e20;
            --light-green: #f4f7f3;
            --dark-earth: #2b2b2b;
            --accent-terracotta: #bd6a42;
            --white: #ffffff;
            --border-color: #e0e6df;
            
            /* Font Variables */
            --font-heading: 'Playfair Display', serif;
            --font-body: 'Inter', sans-serif;
        }

        body {
            color: var(--dark-earth);
            font-family: var(--font-body);
            line-height: 1.7;
            background-color: var(--white);
            -webkit-font-smoothing: antialiased;
        }

        /* Navigation */
        nav {
            background-color: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1.5rem 10%;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 1px 0px rgba(0,0,0,0.05);
        }

        .logo {
            font-family: var(--font-heading);
            font-size: 1.6rem;
            font-weight: 700;
            color: var(--primary-green);
            letter-spacing: -0.5px;
        }

        .nav-links {
            display: flex;
            list-style: none;
        }

        .nav-links li {
            margin-left: 2.5rem;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--dark-earth);
            font-weight: 500;
            font-size: 0.95rem;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: var(--primary-green);
        }

        /* Hero Section */
        header {
            background: linear-gradient(rgba(0, 0, 0, 0.55), rgba(0, 0, 0, 0.55)), url('https://images.unsplash.com/photo-1558271821-3ad2894052a3?auto=format&fit=crop&w=1920&q=80') no-repeat center center/cover;
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: var(--white);
            padding: 0 1rem;
        }

        header h1 {
            font-family: var(--font-heading);
            font-size: 4rem;
            font-weight: 700;
            margin-bottom: 1.5rem;
            max-width: 850px;
            line-height: 1.15;
        }

        header p {
            font-size: 1.25rem;
            font-weight: 300;
            margin-bottom: 2.5rem;
            max-width: 650px;
            opacity: 0.95;
        }

        .btn {
            display: inline-block;
            background-color: var(--accent-terracotta);
            color: var(--white);
            padding: 0.9rem 2.2rem;
            text-decoration: none;
            border-radius: 2px;
            font-weight: 600;
            font-size: 0.95rem;
            letter-spacing: 0.5px;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            font-family: var(--font-body);
        }

        .btn:hover {
            background-color: #a35632;
            transform: translateY(-2px);
        }

        /* Section Global Styling */
        section {
            padding: 6rem 10%;
        }

        h2 {
            font-family: var(--font-heading);
            font-size: 2.8rem;
            font-weight: 700;
            color: var(--primary-green);
            text-align: center;
            margin-bottom: 3.5rem;
        }

        /* The Problem */
        #problem {
            background-color: var(--light-green);
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 2.5rem;
            text-align: center;
        }

        .stat-card {
            background-color: var(--white);
            padding: 3rem 2rem;
            border-radius: 4px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.02);
        }

        .stat-number {
            font-family: var(--font-heading);
            font-size: 4rem;
            font-weight: 700;
            color: var(--accent-terracotta);
            margin-bottom: 0.5rem;
            line-height: 1;
        }

        .stat-card p {
            font-size: 0.95rem;
            color: #555;
        }

        /* Material Breakdown */
        .materials-container {
            max-width: 850px;
            margin: 0 auto;
        }

        .material-row {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 2rem 0;
            border-bottom: 1px solid var(--border-color);
        }

        .material-info h3 {
            font-family: var(--font-heading);
            font-size: 1.4rem;
            color: var(--dark-earth);
            margin-bottom: 0.5rem;
        }

        .material-info p {
            font-size: 0.95rem;
            color: #666;
            max-width: 600px;
        }

        .impact-tag {
            font-family: var(--font-body);
            padding: 0.35rem 1.2rem;
            border-radius: 30px;
            font-size: 0.8rem;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        .high-impact { background-color: #fdf2f2; color: #b82c2c; }
        .med-impact { background-color: #fff8f2; color: #b8622c; }
        .low-impact { background-color: #f2fdf2; color: #2cb849; }

        /* Calculator Section */
        #calculator {
            background-color: var(--white);
        }

        .calc-container {
            max-width: 650px;
            margin: 0 auto;
            background-color: var(--light-green);
            padding: 3rem;
            border-radius: 4px;
        }

        .form-group {
            margin-bottom: 2rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.75rem;
            font-weight: 500;
            font-size: 1rem;
        }

        .form-group select {
            width: 100%;
            padding: 0.9rem;
            border: 1px solid var(--border-color);
            border-radius: 2px;
            font-size: 0.95rem;
            background-color: var(--white);
            font-family: var(--font-body);
            color: var(--dark-earth);
            outline: none;
        }

        .calc-result {
            margin-top: 2.5rem;
            padding-top: 2rem;
            border-top: 1px dashed #b5c4b3;
            text-align: center;
            display: none;
        }

        .calc-result p:first-of-type {
            font-size: 0.9rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            color: #666;
        }

        .result-number {
            font-family: var(--font-heading);
            font-size: 3rem;
            font-weight: 700;
            color: var(--accent-terracotta);
            margin: 0.5rem 0 1rem 0;
        }

        /* Quiz Section */
        #quiz {
            background-color: var(--light-green);
        }

        .quiz-container {
            max-width: 650px;
            margin: 0 auto;
            background-color: var(--white);
            padding: 3rem;
            border-radius: 4px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.02);
        }

        .quiz-question {
            margin-bottom: 2rem;
            padding-bottom: 1.5rem;
            border-bottom: 1px solid var(--border-color);
        }

        .quiz-question:last-of-type {
            border-bottom: none;
        }

        .quiz-question p {
            font-weight: 600;
            font-size: 1.1rem;
            margin-bottom: 1rem;
            color: var(--primary-green);
        }

        .quiz-options {
            display: flex;
            flex-direction: column;
            gap: 0.75rem;
        }

        .quiz-option {
            display: flex;
            align-items: center;
            gap: 0.75rem;
            padding: 0.75rem 1rem;
            border: 1px solid var(--border-color);
            border-radius: 4px;
            cursor: pointer;
            transition: background 0.2s;
        }

        .quiz-option:hover {
            background-color: var(--light-green);
        }

        .quiz-option input {
            cursor: pointer;
        }

        .quiz-feedback {
            margin-top: 2rem;
            padding: 1.5rem;
            border-radius: 4px;
            text-align: center;
            display: none;
            font-weight: 600;
        }

        /* Solutions Section */
        #solutions {
            background-color: var(--white);
        }

        .solutions-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2.5rem;
        }

        .solution-card {
            background: var(--light-green);
            padding: 2.5rem;
            border-radius: 4px;
            border-top: 4px solid var(--primary-green);
        }

        .solution-card h3 {
            font-family: var(--font-heading);
            font-size: 1.4rem;
            margin-bottom: 1rem;
            color: var(--primary-green);
        }

        .solution-card p {
            font-size: 0.95rem;
            color: #555;
        }

        /* Footer */
        footer {
            background-color: var(--dark-earth);
            color: var(--white);
            text-align: center;
            padding: 3rem;
            font-size: 0.9rem;
            letter-spacing: 0.5px;
            opacity: 0.9;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            nav { padding: 1rem 5%; flex-direction: column; }
            .nav-links { margin-top: 1rem; }
            .nav-links li { margin: 0 1rem; }
            header h1 { font-size: 2.6rem; }
            section { padding: 4rem 5%; }
            h2 { font-size: 2.2rem; }
            .material-row { flex-direction: column; align-items: flex-start; gap: 1rem; }
            .calc-container, .quiz-container { padding: 1.5rem; }
        }
    </style>
</head>
<body>

    <nav>
        <div class="logo">NetZeroNow</div>
        <ul class="nav-links">
            <li><a href="#problem">The Problem</a></li>
            <li><a href="#materials">Materials</a></li>
            <li><a href="#calculator">Calculator</a></li>
            <li><a href="#quiz">Quiz</a></li>
            <li><a href="#solutions">Solutions</a></li>
        </ul>
    </nav>

    <header>
        <h1>The True Cost of What We Wear</h1>
        <p>The global textile industry emits more carbon than international flights and maritime shipping combined. It's time to understand the footprint of our clothing.</p>
        <a href="#problem" class="btn">Learn the Facts</a>
    </header>

    <section id="problem">
        <h2>The Global Footprint</h2>
        <div class="stats-grid">
            <div class="stat-card">
                <div class="stat-number">10%</div>
                <p>Of global greenhouse gas emissions are caused by the apparel and textile industry.</p>
            </div>
            <div class="stat-card">
                <div class="stat-number">1.2B</div>
                <p>Tons of CO₂ equivalents released into the atmosphere by global textile production annually.</p>
            </div>
            <div class="stat-card">
                <div class="stat-number">70%</div>
                <p>Of a garment's entire lifecycle emissions come directly from the energy-intensive manufacturing stage.</p>
            </div>
        </div>
    </section>

    <section id="materials">
        <h2>The Carbon Impact of Fibers</h2>
        <div class="materials-container">
            <div class="material-row">
                <div class="material-info">
                    <h3>Polyester & Synthetics</h3>
                    <p>Derived from crude oil, producing synthetic fibers releases heavy amounts of volatile organic compounds and greenhouse gases.</p>
                </div>
                <span class="impact-tag high-impact">High Carbon</span>
            </div>
            <div class="material-row">
                <div class="material-info">
                    <h3>Conventional Cotton</h3>
                    <p>Extremely resource-heavy. High pesticide usage and processing energy lead to a significant footprint.</p>
                </div>
                <span class="impact-tag med-impact">Medium Carbon</span>
            </div>
            <div class="material-row">
                <div class="material-info">
                    <h3>Recycled & Eco-Fibers</h3>
                    <p>Materials like hemp, linen, and recycled cotton require dramatically less land, water, and fossil fuels to create.</p>
                </div>
                <span class="impact-tag low-impact">Low Carbon</span>
            </div>
        </div>
    </section>

    <section id="calculator">
        <h2>Check Your Fashion Footprint</h2>
        <div class="calc-container">
            <div class="form-group">
                <label for="shopping-habits">How many brand-new clothing items do you buy a month?</label>
                <select id="shopping-habits">
                    <option value="0">0 items (I thrift or rarely buy)</option>
                    <option value="1">1 - 2 items</option>
                    <option value="4">3 - 5 items</option>
                    <option value="8">6+ items</option>
                </select>
            </div>

            <div class="form-group">
                <label for="washing-habits">How do you usually wash your clothes?</label>
                <select id="washing-habits">
                    <option value="10">Eco / Cold water (30°C or lower)</option>
                    <option value="40">Standard / Warm water</option>
                </select>
            </div>

            <div class="form-group">
                <label for="drying-habits">How do you dry your clothes?</label>
                <select id="drying-habits">
                    <option value="0">Line dry / Air dry</option>
                    <option value="90">Tumble dryer machine</option>
                </select>
            </div>

            <button onclick="calculateFootprint()" class="btn" style="width: 100%;">Calculate My Impact</button>

            <div id="calc-result" class="calc-result">
                <p>Your estimated annual fashion carbon footprint is:</p>
                <div id="result-number" class="result-number">0 kg CO₂e</div>
                <p id="result-tip" style="font-style: italic; color: #666; font-size: 0.95rem; max-width: 500px; margin: 0 auto;"></p>
            </div>
        </div>
    </section>

    <section id="quiz">
        <h2>Test Your Emissions IQ</h2>
        <div class="quiz-container">
            <form id="emissions-quiz">
                
                <div class="quiz-question">
                    <p>1. Which phase of a garment's life generates the most greenhouse gases?</p>
                    <div class="quiz-options">
                        <label class="quiz-option">
                            <input type="radio" name="q1" value="wrong"> Shipping and transportation
                        </label>
                        <label class="quiz-option">
                            <input type="radio" name="q1" value="correct"> Material processing and manufacturing
                        </label>
                        <label class="quiz-option">
                            <input type="radio" name="q1" value="wrong"> Consumer washing and drying
                        </label>
                    </div>
                </div>

                <div class="quiz-question">
                    <p>2. Synthetic fibers like polyester and nylon are synthesized from which resource?</p>
                    <div class="quiz-options">
                        <label class="quiz-option">
                            <input type="radio" name="q2" value="wrong"> Plant cellulose
                        </label>
                        <label class="quiz-option">
                            <input type="radio" name="q2" value="correct"> Crude oil (Fossil fuels)
                        </label>
                        <label class="quiz-option">
                            <input type="radio" name="q2" value="wrong"> Recycled wood chips
                        </label>
                    </div>
                </div>

                <div class="quiz-question">
                    <p>3. Extending the active lifespan of a piece of clothing by just 9 months reduces its carbon footprint by how much?</p>
                    <div class="quiz-options">
                        <label class="quiz-option">
                            <input type="radio" name="q3" value="wrong"> Around 5%
                        </label>
                        <label class="quiz-option">
                            <input type="radio" name="q3" value="wrong"> Around 50%
                        </label>
                        <label class="quiz-option">
                            <input type="radio" name="q3" value="correct"> Around 20-30%
                        </label>
                    </div>
                </div>

                <button type="button" onclick="evaluateQuiz()" class="btn" style="width: 100%;">Submit Answers</button>
            </form>

            <div id="quiz-feedback" class="quiz-feedback"></div>
        </div>
    </section>

    <section id="solutions">
        <h2>How We Fix It</h2>
        <div class="solutions-grid">
            <div class="solution-card">
                <h3>1. Choose Circular Fashion</h3>
                <p>Extending the life of clothes by just 9 months through thrifting, swapping, and repairing reduces their carbon, water, and waste footprints by around 20-30%.</p>
            </div>
            <div class="solution-card">
                <h3>2. Wash Cold & Air Dry</h3>
                <p>Up to 20% of a garment’s carbon footprint happens at home. Washing clothes at 30°C/86°F and skipping the dryer drastically lowers your household energy use.</p>
            </div>
            <div class="solution-card">
                <h3>3. Demand Transparency</h3>
                <p>Support brands that openly publish their supply chain emissions data and use renewable energy sources in their manufacturing facilities.</p>
            </div>
        </div>
    </section>

    <footer>
        <p>&copy; 2026 NetZeroNow. Spread the word. Change the pattern.</p>
    </footer>

    <script>
        function calculateFootprint() {
            const monthlyItems = parseInt(document.getElementById('shopping-habits').value);
            const washImpact = parseInt(document.getElementById('washing-habits').value);
            const dryImpact = parseInt(document.getElementById('drying-habits').value);

            const annualShoppingImpact = monthlyItems * 12 * 15;
            const totalEmissions = annualShoppingImpact + washImpact + dryImpact;

            document.getElementById('result-number').innerText = totalEmissions + " kg CO₂e / year";
            
            let tip = "";
            if (totalEmissions <= 50) {
                tip = "Amazing job! Your fashion choices are highly sustainable. Keep inspiring others.";
            } else if (totalEmissions <= 250) {
                tip = "Not bad, but room to improve! Try switching to cold washes or swapping one new purchase a month for a thrifted alternative.";
            } else {
                tip = "Your footprint is higher than average. Consider cutting back on new fast-fashion items and air-drying garments to make a massive dent in your total emissions.";
            }
            
            document.getElementById('result-tip').innerText = tip;
            document.getElementById('calc-result').style.display = 'block';
            
            document.getElementById('calc-result').scrollIntoView({ behavior: 'smooth', block: 'nearest' });
        }

        function evaluateQuiz() {
            const quizForm = document.getElementById('emissions-quiz');
            const feedbackDiv = document.getElementById('quiz-feedback');
            
            const q1 = quizForm.elements['q1'].value;
            const q2 = quizForm.elements['q2'].value;
            const q3 = quizForm.elements['q3'].value;

            if (!q1 || !q2 || !q3) {
                feedbackDiv.style.display = 'block';
                feedbackDiv.style.backgroundColor = '#fff3e6';
                feedbackDiv.style.color = '#cc6600';
                feedbackDiv.innerText = "Please answer all questions before submitting!";
                return;
            }

            let score = 0;
            if (q1 === 'correct') score++;
            if (q2 === 'correct') score++;
            if (q3 === 'correct') score++;

            feedbackDiv.style.display = 'block';
            
            if (score === 3) {
                feedbackDiv.style.backgroundColor = '#f2fdf2';
                feedbackDiv.style.color = '#2cb849';
                feedbackDiv.innerText = "Perfect Score! 3/3. You are a true sustainable fashion expert.";
            } else if (score === 2) {
                feedbackDiv.style.backgroundColor = '#fff8f2';
                feedbackDiv.style.color = '#b8622c';
                feedbackDiv.innerText = "Great job! 2/3. You have a solid understanding of textile emissions.";
            } else {
                feedbackDiv.style.backgroundColor = '#fdf2f2';
                feedbackDiv.style.color = '#b82c2c';
                feedbackDiv.innerText = `You scored ${score}/3. Review the facts above on materials and manufacturing to learn more!`;
            }

            feedbackDiv.scrollIntoView({ behavior: 'smooth', block: 'nearest' });
        }
    </script>

</body>
</html>
