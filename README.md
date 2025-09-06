<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Louis Pasteur: The Germ Hunter Infographic</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;700;900&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
        }
        .chart-container {
            position: relative;
            width: 100%;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
            height: 300px;
            max-height: 400px;
        }
        @media (min-width: 768px) {
            .chart-container {
                height: 350px;
            }
        }
        .flow-arrow::after {
            content: '▼';
            font-size: 2rem;
            color: #118AB2;
            display: block;
            text-align: center;
            margin: 0.5rem 0;
        }
        .flow-box {
            border: 2px solid #118AB2;
        }
    </style>
</head>
<body class="bg-gray-100 text-[#073B4C]">
    <div class="container mx-auto p-4 md:p-8">

        <header class="text-center mb-12">
            <h1 class="text-4xl md:text-6xl font-black text-[#073B4C] mb-2">Louis Pasteur</h1>
            <p class="text-xl md:text-2xl text-[#118AB2]">The Scientist Who Changed Our World</p>
        </header>

        <main class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">

            <div class="md:col-span-1 lg:col-span-1 bg-white rounded-lg shadow-lg p-6 flex flex-col justify-center items-center text-center">
                <h2 class="text-2xl font-bold text-[#118AB2] mb-2">An Unlikely Start</h2>
                <p class="text-6xl font-black text-[#FF6B6B]">1822</p>
                <p class="mt-2 font-bold">Born in Dole, France</p>
                <p class="mt-4">He wasn't a star student at first and even found chemistry difficult! His journey shows that dedication can lead to greatness, even if you don't start at the top.</p>
            </div>

            <div class="md:col-span-2 lg:col-span-2 bg-white rounded-lg shadow-lg p-6">
                <h2 class="text-2xl font-bold text-center text-[#118AB2] mb-4">The Secret of Fermentation</h2>
                <p class="text-center mb-6">Before Pasteur, people were puzzled by how things like grape juice turned into wine. Pasteur discovered it wasn't magic, but tiny living things called microorganisms! He showed that different microbes have different effects.</p>
                <div class="flex flex-col md:flex-row justify-around items-center text-center">
                    <div class="mb-4 md:mb-0">
                        <div class="text-6xl mb-2">😊</div>
                        <h3 class="text-xl font-bold text-[#06D6A0]">Good Microbes</h3>
                        <p>Yeast turns grape juice into delicious wine.</p>
                    </div>
                    <div class="text-2xl font-bold text-gray-300 mx-4">+</div>
                    <div>
                        <div class="text-6xl mb-2">😠</div>
                        <h3 class="text-xl font-bold text-[#FF6B6B]">Bad Microbes</h3>
                        <p>Other bacteria can make it turn sour and spoil.</p>
                    </div>
                </div>
                <p class="mt-6 text-center font-semibold">This led to his famous invention, **Pasteurization**, where gentle heating kills bad microbes in milk and other drinks to keep them safe!</p>
            </div>

            <div class="md:col-span-2 lg:col-span-3 bg-white rounded-lg shadow-lg p-6">
                <h2 class="text-2xl font-bold text-center text-[#118AB2] mb-4">Busting a 2,000-Year-Old Myth</h2>
                <p class="text-center mb-6">For centuries, people believed in "spontaneous generation"—the idea that life could just appear from non-living things. Pasteur proved this wrong with a brilliant and simple experiment.</p>
                <div class="flex flex-col items-center">
                    <div class="w-full max-w-sm p-4 rounded-lg flow-box text-center">
                        <h3 class="font-bold">1. Broth is Boiled</h3>
                        <p>Nutrient broth is boiled in a special S-neck flask, killing any existing microbes.</p>
                    </div>
                    <div class="flow-arrow"></div>
                    <div class="w-full max-w-sm p-4 rounded-lg flow-box text-center">
                        <h3 class="font-bold">2. Flask is Left to Cool</h3>
                        <p>The S-shape lets air in but traps airborne dust and microbes in the bend.</p>
                    </div>
                    <div class="flow-arrow"></div>
                    <div class="w-full max-w-sm p-4 rounded-lg bg-[#06D6A0] text-white text-center">
                        <h3 class="font-bold">RESULT: No Growth!</h3>
                        <p>For a long time, the broth remains clear. No life appears!</p>
                    </div>
                     <div class="flow-arrow"></div>
                    <div class="w-full max-w-sm p-4 rounded-lg flow-box text-center">
                         <h3 class="font-bold">3. Flask is Tilted</h3>
                        <p>When the flask is tilted, the trapped microbes wash into the broth.</p>
                    </div>
                    <div class="flow-arrow"></div>
                    <div class="w-full max-w-sm p-4 rounded-lg bg-[#FF6B6B] text-white text-center">
                        <h3 class="font-bold">RESULT: Growth!</h3>
                        <p>Soon, the broth becomes cloudy with microbial growth. Life comes from other life!</p>
                    </div>
                </div>
            </div>

            <div class="md:col-span-2 lg:col-span-3 bg-white rounded-lg shadow-lg p-6">
                <h2 class="text-2xl font-bold text-center text-[#118AB2] mb-4">The Vaccine Revolution</h2>
                <p class="text-center mb-6">Pasteur's work on germs led to his greatest contribution to humanity: the development of vaccines. By studying weakened forms of germs, he found a way to train the body to fight off deadly diseases.</p>
                <div class="chart-container">
                    <canvas id="vaccineTimeline"></canvas>
                </div>
                <p class="text-center mt-4">His most famous success was saving 9-year-old Joseph Meister from rabies, proving that his vaccine worked in humans and saving countless lives since.</p>
            </div>

            <!-- Gemini API Section -->
            <div class="md:col-span-2 lg:col-span-3 bg-white rounded-lg shadow-lg p-6 flex flex-col items-center">
                <h2 class="text-2xl font-bold text-center text-[#118AB2] mb-4">✨ Ask Pasteur: Powered by Gemini ✨</h2>
                <p class="text-center text-lg mb-4">What else would you like to know about Louis Pasteur?</p>
                <textarea id="ask-input" class="w-full h-24 p-4 border rounded-lg resize-none mb-4 focus:outline-none focus:ring-2 focus:ring-[#118AB2]" placeholder="e.g., How did he discover the rabies vaccine?"></textarea>
                <button id="ask-button" class="w-full md:w-auto px-6 py-3 bg-[#06D6A0] text-white font-bold rounded-lg shadow-md hover:bg-[#05a37f] transition-colors">Ask</button>
                <div id="ask-output" class="mt-6 w-full p-4 bg-gray-50 rounded-lg hidden">
                    <div id="loading" class="text-center text-[#118AB2] hidden">
                        <p>Thinking...</p>
                    </div>
                    <div id="answer" class="text-gray-700"></div>
                    <div id="citations" class="text-xs text-gray-500 mt-4"></div>
                </div>
            </div>

        </main>

        <footer class="text-center mt-12 py-6 border-t-2 border-[#118AB2]">
            <p class="text-lg font-bold text-[#073B4C]">Louis Pasteur's legacy lives on in every safe glass of milk, every life-saving vaccine, and our modern understanding of medicine.</p>
        </footer>
    </div>

    <script>
        function wrapLabel(str, maxWidth) {
            if (str.length <= maxWidth) {
                return str;
            }
            const words = str.split(' ');
            let lines = [];
            let currentLine = words[0];
            for (let i = 1; i < words.length; i++) {
                if (currentLine.length + words[i].length + 1 <= maxWidth) {
                    currentLine += ' ' + words[i];
                } else {
                    lines.push(currentLine);
                    currentLine = words[i];
                }
            }
            lines.push(currentLine);
            return lines;
        }
        
        const rawLabels = ['1879: Chicken Cholera Vaccine Discovery', '1881: Anthrax Vaccine Public Trial', '1885: First Human Rabies Vaccination'];
        const processedLabels = rawLabels.map(label => wrapLabel(label, 16));

        const ctx = document.getElementById('vaccineTimeline').getContext('2d');
        const vaccineTimeline = new Chart(ctx, {
            type: 'line',
            data: {
                labels: processedLabels,
                datasets: [{
                    label: 'Key Vaccine Milestones',
                    data: [1, 2, 3],
                    backgroundColor: 'rgba(6, 214, 160, 0.2)',
                    borderColor: '#06D6A0',
                    borderWidth: 3,
                    fill: true,
                    tension: 0.1,
                    pointBackgroundColor: '#118AB2',
                    pointRadius: 6,
                    pointHoverRadius: 8
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                scales: {
                    y: {
                        beginAtZero: true,
                        ticks: {
                            display: false
                        },
                        grid: {
                           display: false
                        }
                    },
                    x: {
                        grid: {
                            display: false
                        }
                    }
                },
                plugins: {
                    legend: {
                        display: false
                    },
                    tooltip: {
                        callbacks: {
                            title: function(tooltipItems) {
                                const item = tooltipItems[0];
                                let label = item.chart.data.labels[item.dataIndex];
                                if (Array.isArray(label)) {
                                  return label.join(' ');
                                } else {
                                  return label;
                                }
                            }
                        }
                    }
                }
            }
        });

        document.getElementById('ask-button').addEventListener('click', askPasteur);

        async function askPasteur() {
            const query = document.getElementById('ask-input').value;
            const outputDiv = document.getElementById('ask-output');
            const loadingDiv = document.getElementById('loading');
            const answerDiv = document.getElementById('answer');
            const citationsDiv = document.getElementById('citations');

            outputDiv.style.display = 'block';
            loadingDiv.style.display = 'block';
            answerDiv.textContent = '';
            citationsDiv.textContent = '';

            const systemPrompt = "You are a historical expert on the life and discoveries of Louis Pasteur. Provide a concise, single-paragraph summary in a friendly and educational tone. Ensure your answer is factually accurate.";
            const apiKey = "";
            const apiUrl = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash-preview-05-20:generateContent?key=${apiKey}`;

            const payload = {
                contents: [{ parts: [{ text: query }] }],
                tools: [{ "google_search": {} }],
                systemInstruction: {
                    parts: [{ text: systemPrompt }]
                }
            };

            const response = await fetch(apiUrl, {
                method: 'POST',
                headers: { 'Content-Type': 'application/json' },
                body: JSON.stringify(payload)
            });

            const result = await response.json();
            loadingDiv.style.display = 'none';

            const candidate = result.candidates?.[0];
            if (candidate && candidate.content?.parts?.[0]?.text) {
                const text = candidate.content.parts[0].text;
                answerDiv.textContent = text;
                
                const groundingMetadata = candidate.groundingMetadata;
                if (groundingMetadata && groundingMetadata.groundingAttributions) {
                    const sources = groundingMetadata.groundingAttributions
                        .map(attribution => ({
                            uri: attribution.web?.uri,
                            title: attribution.web?.title,
                        }))
                        .filter(source => source.uri && source.title);

                    if (sources.length > 0) {
                        citationsDiv.innerHTML = '<strong>Sources:</strong><ul>' + 
                            sources.map(s => `<li><a href="${s.uri}" target="_blank" class="text-[#118AB2] hover:underline">${s.title}</a></li>`).join('') +
                            '</ul>';
                    }
                }
            } else {
                answerDiv.textContent = 'Sorry, I could not find a suitable answer. Please try a different question.';
            }
        }
    </script>
</body>
</html>
  
