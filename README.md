# Cv_professionnel
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Générateur de CV</title>
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <script defer src="script.js"></script>
</head>
<body class="bg-gray-100 p-6">
    <div class="max-w-4xl mx-auto bg-white shadow-lg rounded-lg p-6">
        <h2 class="text-2xl font-bold text-center text-blue-600">📝 Générateur de CV</h2>

        <!-- Formulaire -->
        <form id="cv-form" class="mt-4">
            <div class="mb-4">
                <label class="block text-gray-700 font-bold">Nom et Prénom :</label>
                <input type="text" id="nomPrenom" class="w-full p-2 border rounded" required>
            </div>

            <div class="mb-4">
                <label class="block text-gray-700 font-bold">Email :</label>
                <input type="email" id="email" class="w-full p-2 border rounded" required>
            </div>

            <div class="mb-4">
                <label class="block text-gray-700 font-bold">Téléphone :</label>
                <input type="text" id="telephone" class="w-full p-2 border rounded" required>
            </div>

            <div class="mb-4">
                <label class="block text-gray-700 font-bold">Compétences :</label>
                <textarea id="competences" class="w-full p-2 border rounded"></textarea>
            </div>

            <div class="mb-4">
                <label class="block text-gray-700 font-bold">Expérience :</label>
                <textarea id="experience" class="w-full p-2 border rounded"></textarea>
            </div>

            <button type="button" id="genererCV" class="bg-blue-500 text-white p-2 rounded w-full mt-2">
                Générer CV
            </button>
        </form>
    </div>

    <!-- Prévisualisation -->
    <div class="max-w-4xl mx-auto bg-white shadow-lg rounded-lg p-6 mt-6" id="cv-preview">
        <h2 class="text-2xl font-bold text-gray-800" id="preview-nom"></h2>
        <p class="text-gray-600" id="preview-email"></p>
        <p class="text-gray-600" id="preview-telephone"></p>
        <h3 class="text-xl font-bold mt-4">Compétences :</h3>
        <p id="preview-competences"></p>
        <h3 class="text-xl font-bold mt-4">Expérience :</h3>
        <p id="preview-experience"></p>
        <button id="downloadPDF" class="bg-green-500 text-white p-2 rounded mt-4">
            Télécharger en PDF
        </button>
    </div>

    <script>
        $(document).ready(function() {
            $('#genererCV').click(function() {
                $('#preview-nom').text($('#nomPrenom').val());
                $('#preview-email').text($('#email').val());
                $('#preview-telephone').text($('#telephone').val());
                $('#preview-competences').text($('#competences').val());
                $('#preview-experience').text($('#experience').val());
            });
        });
    </script>
</body>
</html>
