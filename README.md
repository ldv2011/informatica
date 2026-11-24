<!DOCTYPE html>
<html lang="nl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>De beste website</title>
    <!-- Tailwind CSS voor de mooie kleuren en opmaak -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Styling om pagina's te verbergen en te tonen */
        .page {
            display: none;
        }
        .page.active {
            display: block;
        }
    </style>
</head>
<body class="bg-indigo-50 text-indigo-900 p-4 md:p-10 font-sans max-w-2xl mx-auto">

    <!-- Navigatie menu -->
    <header class="mb-8 border-b border-indigo-200 pb-4">
        <h1 class="text-4xl font-extrabold mb-4 text-indigo-700 drop-shadow-sm">De beste website</h1>
        <nav class="flex flex-wrap gap-3">
            <button onclick="toonPagina('home')" class="bg-indigo-200 text-indigo-800 px-4 py-2 rounded-lg hover:bg-indigo-300 font-semibold transition shadow-sm">Home</button>
            <button onclick="toonPagina('wie-ben-ik')" class="bg-indigo-200 text-indigo-800 px-4 py-2 rounded-lg hover:bg-indigo-300 font-semibold transition shadow-sm">Wie ben ik</button>
            <button onclick="toonPagina('hobbys')" class="bg-indigo-200 text-indigo-800 px-4 py-2 rounded-lg hover:bg-indigo-300 font-semibold transition shadow-sm">Hobby's</button>
            <button onclick="toonPagina('extra')" class="bg-indigo-200 text-indigo-800 px-4 py-2 rounded-lg hover:bg-indigo-300 font-semibold transition shadow-sm">Meer over mij</button>
        </nav>
    </header>

    <!-- De content van de website -->
    <main class="bg-white p-6 rounded-xl shadow-md border border-indigo-100">
        <!-- Pagina 1: Home -->
        <div id="home" class="page active">
            <h2 class="text-2xl font-bold mb-2 text-indigo-600">Welkom!</h2>
            <p>Dit is de homepagina van mijn website. Zoals je ziet is hij expres heel simpel gehouden, zonder te veel poespas of moeilijke designs.</p>
            <br>
            <p>Klik op de linkjes hierboven om naar de andere pagina's te gaan.</p>
        </div>

        <!-- Pagina 2: Wie ben ik -->
        <div id="wie-ben-ik" class="page">
            <h2 class="text-2xl font-bold mb-2 text-indigo-600">Wie ben ik?</h2>
            <p>Hallo! Ik ben de maker van deze website.</p>
            <p>Hier kun je wat meer informatie over jezelf opschrijven, zoals hoe oud je bent, waar je woont of wat je in het dagelijks leven doet.</p>
        </div>

        <!-- Pagina 3: Hobby's -->
        <div id="hobbys" class="page">
            <h2 class="text-2xl font-bold mb-2 text-indigo-600">Mijn Hobby's</h2>
            <p>In mijn vrije tijd doe ik graag de volgende dingen:</p>
            <ul class="list-disc ml-6 mt-2">
                <li>Gamen</li>
                <li>Muziek luisteren</li>
                <li>Sporten</li>
                <li>Afspreken met vrienden</li>
            </ul>
            <br>
            <p>(Je kunt deze lijst natuurlijk aanpassen naar je eigen hobby's!)</p>
        </div>

        <!-- Pagina 4: Extra informatie -->
        <div id="extra" class="page">
            <h2 class="text-2xl font-bold mb-2 text-indigo-600">Nog wat extra over mij</h2>
            <p>Leuk dat je tot hier bent doorgeklikt!</p>
            <p>Mijn favoriete eten is pizza en ik hou van dieren. Dit was mijn simpele website, bedankt voor het bezoeken.</p>
        </div>
    </main>

    <!-- Script om tussen de pagina's te wisselen -->
    <script>
        function toonPagina(paginaId) {
            // Verberg alle pagina's
            const paginas = document.querySelectorAll('.page');
            paginas.forEach(pagina => {
                pagina.classList.remove('active');
            });

            // Toon de gekozen pagina
            const gekozenPagina = document.getElementById(paginaId);
            if(gekozenPagina) {
                gekozenPagina.classList.add('active');
            }
        }
    </script>
</body>
</html>
