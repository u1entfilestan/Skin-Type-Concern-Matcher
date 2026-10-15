<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Skin Type & Concern Matcher</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,500;0,600;0,700;1,400&family=Plus+Jakarta+Sans:wght@400;500;600&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Plus Jakarta Sans', sans-serif;
    }
    .font-serif-custom {
      font-family: 'Playfair Display', serif;
    }
  </style>
</head>
<body class="bg-transparent flex items-center justify-center min-h-screen p-4">

  <div class="w-full max-w-2xl bg-white rounded-3xl p-6 sm:p-10 shadow-sm border border-pink-50 text-center relative overflow-hidden">
    
    <!-- Header -->
    <div class="mb-8">
      <span class="text-xs font-semibold tracking-widest text-[#E39695] uppercase block mb-2">Personalized Recommendation</span>
      <h1 class="font-serif-custom text-3xl sm:text-4xl font-semibold text-[#1E293B] mb-3">Skin Type & Concern Matcher</h1>
      <p class="text-gray-500 text-sm sm:text-base max-w-md mx-auto">Filter our handpicked K-Beauty holy grails according to your exact skin profile.</p>
    </div>

    <!-- Section 1: Skin Type -->
    <div class="mb-8 text-left">
      <div class="flex items-center gap-2 mb-4">
        <span class="w-6 h-6 rounded-full bg-[#FCE7E6] text-[#D16B6A] text-xs font-bold flex items-center justify-center">1</span>
        <h2 class="text-xs font-bold tracking-wider text-[#1E293B] uppercase">Select Your Skin Type</h2>
      </div>
      <div id="skin-types" class="grid grid-cols-2 sm:grid-cols-3 gap-3"></div>
    </div>

    <!-- Section 2: Primary Skin Concern -->
    <div class="mb-6 text-left">
      <div class="flex items-center gap-2 mb-4">
        <span class="w-6 h-6 rounded-full bg-[#FCE7E6] text-[#D16B6A] text-xs font-bold flex items-center justify-center">2</span>
        <h2 class="text-xs font-bold tracking-wider text-[#1E293B] uppercase">Primary Skin Concern</h2>
      </div>
      <div id="skin-concerns" class="grid grid-cols-1 sm:grid-cols-2 gap-3"></div>
    </div>

  </div>

  <script>
    const skinTypes = ["All Types", "Oily", "Dry", "Combination", "Sensitive", "Normal"];
    const skinConcerns = ["All Concerns", "Acne & Blemishes", "Brightening & Tone", "Hydration & Barrier"];

    let selectedType = "All Types";
    let selectedConcern = "All Concerns";

    function renderButtons() {
      const typeContainer = document.getElementById('skin-types');
      typeContainer.innerHTML = '';
      skinTypes.forEach(type => {
        const isSelected = selectedType === type;
        const btn = document.createElement('button');
        btn.className = `py-3 px-4 rounded-xl text-sm font-medium transition-all duration-200 border text-center ${
          isSelected 
            ? 'bg-[#FFF5F5] border-[#E8A5A5] text-[#D16B6A] shadow-sm' 
            : 'bg-white border-gray-200 text-gray-700 hover:border-gray-300'
        }`;
        btn.textContent = type;
        btn.onclick = () => {
          selectedType = type;
          renderButtons();
        };
        typeContainer.appendChild(btn);
      });

      const concernContainer = document.getElementById('skin-concerns');
      concernContainer.innerHTML = '';
      skinConcerns.forEach(concern => {
        const isSelected = selectedConcern === concern;
        const btn = document.createElement('button');
        btn.className = `py-3 px-4 rounded-xl text-sm font-medium transition-all duration-200 border text-center ${
          isSelected 
            ? 'bg-[#FFF5F5] border-[#E8A5A5] text-[#D16B6A] shadow-sm' 
            : 'bg-white border-gray-200 text-gray-700 hover:border-gray-300'
        }`;
        btn.textContent = concern;
        btn.onclick = () => {
          selectedConcern = concern;
          renderButtons();
        };
        concernContainer.appendChild(btn);
      });
    }

    renderButtons();
  </script>
</body>
</html>
