

https://github.com/user-attachments/assets/dc84800b-0413-4058-9975-57b854826f18

# it-course-somali
IT Course in Somali language – beginner to intermediate level, including hardware, software, networking, and security basics.


<!DOCTYPE html>
<html lang="so">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Giftuhub Academy Admin Portal</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Tani waxay hubinaysaa in qoodhku uusan u muuqan qoraal caadi ah */
        body { margin: 0; padding: 0; overflow-x: hidden; background-color: #f1f5f9; }
        .active-tab { border-bottom: 4px solid #2563eb; color: #2563eb; }
    </style>
</head>
<body class="bg-slate-50">

    <!-- Navbar -->
    <nav class="bg-white shadow-md p-4 sticky top-0 z-50">
        <div class="container mx-auto flex justify-between items-center">
            <h1 class="text-2xl font-black text-blue-600 tracking-tighter">GIFTUHUB <span class="text-slate-800">ACADEMY</span></h1>
            <div class="flex gap-4">
                <button onclick="nav('home')" class="font-bold text-sm text-slate-600 hover:text-blue-600 transition">Hoyga</button>
                <button onclick="nav('course')" class="font-bold text-sm text-slate-600 hover:text-blue-600 transition">Casharrada</button>
                <button onclick="nav('admin')" class="bg-blue-600 text-white px-4 py-2 rounded-lg text-sm font-bold shadow-lg shadow-blue-200">Admin Mode</button>
            </div>
        </div>
    </nav>

    <!-- Main Container -->
    <div id="content" class="container mx-auto p-6 min-h-screen">
        <!-- Content will be injected here by JS -->
    </div>

    <script>
        // State Management
        let state = 'home';

        function render() {
            const root = document.getElementById('content');
            if(state === 'home') {
                root.innerHTML = `
                    <div class="flex flex-col items-center text-center py-20 animate-fade-in">
                        <i class="fas fa-robot text-8xl text-blue-600 mb-6 opacity-20"></i>
                        <h2 class="text-5xl font-black text-slate-800 mb-4 tracking-tight">Maamul Giftuhub Academy</h2>
                        <p class="text-slate-500 max-w-xl text-lg mb-8">Kani waa dashboard-kaaga rasmiga ah. Halkan ka maamul casharrada, AI animations-ka, iyo scripts-ka.</p>
                        <button onclick="nav('course')" class="bg-slate-900 text-white px-10 py-4 rounded-2xl font-bold hover:bg-blue-600 transition">Bilow Shaqada</button>
                    </div>
                `;
            } else if(state === 'course') {
                root.innerHTML = `
                    <div class="grid md:grid-cols-3 gap-6">
                        <div class="bg-white p-6 rounded-3xl shadow-sm border border-slate-100">
                            <i class="fas fa-microchip text-3xl text-blue-500 mb-4"></i>
                            <h3 class="font-bold text-xl mb-2">Lesson 1: Hardware</h3>
                            <p class="text-sm text-slate-500 mb-4">Mawduucyada Hardware & Software ee Phase 1.</p>
                            <button class="text-blue-600 font-bold text-sm">Eeg Script-ga &rarr;</button>
                        </div>
                        <div class="bg-white p-6 rounded-3xl shadow-sm border border-slate-100">
                            <i class="fas fa-globe text-3xl text-indigo-500 mb-4"></i>
                            <h3 class="font-bold text-xl mb-2">Lesson 2: Internet</h3>
                            <p class="text-sm text-slate-500 mb-4">Barashada Internetka iyo Email-lada.</p>
                            <button class="text-indigo-600 font-bold text-sm">Eeg Script-ga &rarr;</button>
                        </div>
                        <div class="bg-white p-6 rounded-3xl shadow-sm border border-slate-100">
                            <i class="fas fa-file-invoice text-3xl text-orange-500 mb-4"></i>
                            <h3 class="font-bold text-xl mb-2">Lesson 3: Office</h3>
                            <p class="text-sm text-slate-500 mb-4">MS Word, Excel, iyo PowerPoint basics.</p>
                            <button class="text-orange-600 font-bold text-sm">Eeg Script-ga &rarr;</button>
                        </div>
                    </div>
                `;
            }
        }

        function nav(s) {
            state = s;
            render();
        }

        // Initial Render
        window.onload = render;
    </script>
</body>
</html>
