<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>DAVI - Profile</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        body {
            cursor: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewport="0 0 100 100" style="fill:rgba(74, 222, 128, 1);font-size:16px;"><text y="50%">█</text></svg>'), auto;
        }
        .scanline::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            width: 100%; 
            height: 100%;
            background: repeating-linear-gradient(
                0deg,
                rgba(0, 0, 0, 0) 0,
                rgba(0, 0, 0, 0.3) 1.5px,
                rgba(0, 0, 0, 0) 3px
            );
            pointer-events: none;
        }
        .glitch-text::before, .glitch-text::after {
            content: attr(data-text);
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            overflow: hidden;
            background: #000;
        }
        .glitch-text::before {
            left: 3px;
            text-shadow: -2px 0 #ff00c1;
            animation: glitch-anim-1 2.5s linear infinite reverse;
        }
        .glitch-text::after {
            left: -3px;
            text-shadow: -2px 0 #00fff9, 2px 2px #ff00c1;
            animation: glitch-anim-2 1.5s linear infinite reverse;
        }
        @keyframes glitch-anim-1 {
            0% { clip-path: inset(15% 0 86% 0); transform: translate(-5px, 0); }
            10% { clip-path: inset(54% 0 1% 0); transform: translate(5px, 0); }
            20% { clip-path: inset(89% 0 9% 0); }
            30% { clip-path: inset(23% 0 43% 0); transform: translate(-3px, 0); }
            40% { clip-path: inset(34% 0 45% 0); }
            50% { clip-path: inset(1% 0 95% 0); transform: translate(4px, 0); }
            60% { clip-path: inset(78% 0 18% 0); }
            70% { clip-path: inset(48% 0 47% 0); transform: translate(-5px, 0); }
            80% { clip-path: inset(93% 0 3% 0); }
            90% { clip-path: inset(45% 0 48% 0); transform: translate(3px, 0); }
            100% { clip-path: inset(23% 0 76% 0); }
        }
        @keyframes glitch-anim-2 {
            0% { clip-path: inset(83% 0 3% 0); transform: translate(5px, 0); }
            10% { clip-path: inset(45% 0 54% 0); transform: translate(-5px, 0); }
            20% { clip-path: inset(5% 0 92% 0); }
            30% { clip-path: inset(67% 0 18% 0); transform: translate(3px, 0); }
            40% { clip-path: inset(21% 0 77% 0); }
            50% { clip-path: inset(88% 0 1% 0); transform: translate(-4px, 0); }
            60% { clip-path: inset(39% 0 57% 0); }
            70% { clip-path: inset(99% 0 1% 0); transform: translate(5px, 0); }
            80% { clip-path: inset(18% 0 81% 0); }
            90% { clip-path: inset(74% 0 2% 0); transform: translate(-3px, 0); }
            100% { clip-path: inset(49% 0 49% 0); }
        }
    </style>
</head>
<body class="bg-black">
    <main class="min-h-screen bg-black text-green-400 font-mono flex flex-col items-center justify-center text-center p-4 overflow-hidden select-none relative scanline">
      <!-- Background grid pattern -->
      <div 
        class="absolute inset-0 bg-black opacity-20" 
        style="background-image: linear-gradient(rgba(74, 222, 128, 0.3) 1px, transparent 1px), linear-gradient(to right, rgba(74, 222, 128, 0.3) 1px, black 1px); background-size: 2rem 2rem;"
      ></div>

      <div class="z-10 relative">
        <!-- The main name text with the glitch effect applied via CSS -->
        <h1 class="relative text-[12rem] font-black leading-none glitch-text" data-text="DAVI">
          DAVI
        </h1>

        <p class="text-2xl mt-4 uppercase tracking-[.5em]" style="text-shadow: 0 0 5px #22c55e;">
          Software Developer
        </p>
        
        <div class="mt-8 space-y-2 text-left max-w-lg mx-auto">
          <p class="text-lg text-cyan-400">
            <span class="animate-pulse">&gt;</span> STATUS: CONNECTION ESTABLISHED.
          </p>
          <p class="text-md text-gray-500">
            &gt; LOADING PROFILE MODULES... <span class="text-green-500">[OK]</span>
          </p>
          <p class="text-md text-gray-500">
            &gt; WELCOME TO MY TERMINAL.
          </p>
        </div>
        
        <!-- Link to GitHub with themed styling and hover effects -->
        <a 
          href="https://github.com/davialves"
          target="_blank"
          rel="noopener noreferrer"
          class="mt-12 inline-block px-8 py-3 border-2 border-green-400 text-green-400 uppercase tracking-widest transition-all duration-300 hover:bg-green-400 hover:text-black hover:shadow-[0_0_25px_#22c55e] focus:outline-none focus:ring-2 focus:ring-green-400 focus:ring-offset-2 focus:ring-offset-black"
        >
          GitHub
        </a>
      </div>
    </main>
</body>
</html>
