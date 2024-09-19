<script>
    import Step from "./Step.svelte";

    let steps = [
        {name: 'Movie recommendation based on Netflix customer reviews', icon:'fa-solid fa-clapperboard',href:"https://www.google.com"},
        {name: 'Chess engine', icon:'fa-solid fa-chess-board',href:"https://www.google.com"},
        {name: 'StrasMemory', icon:'fa-solid fa-map-location-dot',href:"https://strasmemory.lucasmarchand.dev/"},
        {name: 'TCP clients-proxy-server communication with error detection', icon:'fa-solid fa-server',href:"https://www.google.com"},
        {name: '2D and 3D Games with UE4', icon:'fa-solid fa-gamepad',href:"#"},
        {name: 'Creation of a physics engine', icon:'fa-solid fa-scale-unbalanced',href:"#"},

    ]

    import TableRow from "./TableRow.svelte";   

    let rows = [
        {
            title: 'Game Development',
            icons: [
                { src: 'images/icons/unrealengine.svg', alt: 'Unreal Engine 4' },
                { src: 'images/icons/sdl.svg', alt: 'SDL2' },
                { src: 'images/icons/cplusplus.svg', alt: 'C++' },
                { src: 'images/icons/unity.svg', alt: 'Unity (Clicker app)' },
                { src: 'images/icons/c.svg', alt: 'Love2D' },
                { src: 'images/icons/sfml.svg', alt: 'SFML' }
            ]
        },
        {
            title: 'Web Development',
            icons: [
                { src: 'images/icons/html5.svg', alt: 'HTML' },
                { src: 'images/icons/css3.svg', alt: 'CSS' },
                { src: 'images/icons/javascript.svg', alt: 'JavaScript' },
                { src: 'images/icons/svelte.svg', alt: 'Svelte' }
            ]
        },
        {
            title: 'Artificial Intelligence',
            icons: [
                { src: 'images/icons/python.svg', alt: 'Python3' },
                { src: 'images/icons/tensorflow.svg', alt: 'Tensorflow' },
                { src: 'images/icons/numpy.svg', alt: 'Numpy' }
            ]
        },
    ];

</script>

<main class="flex flex-col flex-1 p-4">
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
        <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                Hi! I'm <span class="poppins text-violet-400">Lucas</span> Marchand <br/>
                <span class="poppins text-violet-400"> AI Student</span> 
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                Bla <span class="text-violet-400">Blabla</span> Blablabla <br/>
                Lorem ipsum dolor, sit amet consectetur adipisicing elit. Magnam animi ducimus dolorem possimus eum adipisci excepturi maiores facilis magni modi?
            </p>
        </div>
        <div class="relative shadow-2xl grid place-items-center">
            <img src={"images/pp.webp"} alt="Profile image" class="object-cover z-[2] max-h-[70vh]"/>
        </div>
    </section>


    <section id="projets" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class = "flex flex-col gap-2 text-center">
            <h6 class="text-lg sm:text-xl md:text-2xl">
                <p class="underline">Mes projets :</p>
            </h6>
        </div>

        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>My project provides personalized movie recommendations by analyzing Netflix customer reviews. Using feedback and sentiment analysis, the system suggests films that match individual preferences and viewing habits.
                </p>
            </Step>
            
            <Step step={steps[1]}>
                <p>My project is a chess engine that lets users play without worrying about the rules, automatically handling legal moves. It can also be easily modified to power a bot that plays chess autonomously.
                    <!--<strong class="text-violet-400">Mettre des choses importantes</strong>-->
                </p>
            </Step>
            
            <Step step={steps[2]}>
                <p>StrasMemory is a web-based game where players have to find tram stops in Strasbourg. It combines fun and geography, challenging users to locate the city's tram stops on a map.
                </p>
            </Step>

            <Step step={steps[3]}>
                <p>TCP clients-proxy-server communication involves clients connecting to a server through a proxy, with error detection mechanisms ensuring data integrity during transmission.
                </p>
            </Step>
            
            <Step step={steps[4]}>
                <p>With UE4, I've developed a 2D Mario-like game and a small 3D zombie survival game similar to Call of Duty: Black Ops.
                </p>
            </Step>

            <Step step={steps[5]}>
                <p>I'm developing a physics engine from scratch to better understand physics simulations, using the book <i>Game Physics Engine Development</i> by Ian Millington as a key reference.</p>
            </Step>
        </div>
    </section>

    <section id="Expérience" class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative">
        <div class = "flex flex-col gap-2 text-center">
            <h6 class="text-lg sm:text-xl md:text-2xl">
                <p class="underline">Mon Expérience :</p>
            </h6>
        </div>

        
        {#each rows as row}
        <TableRow title={row.title} icons={row.icons} />
        <hr class="h-px bg-gray-200 border-0 dark:bg-gray-700">
        {/each}
    </section>
    <section id="cv" class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col items-center gap-8 bg-slate-50">
        <h2 class="text-2xl sm:text-3xl md:text-4xl font-bold text-center">
            Download my resume
        </h2>
    
        <div class="flex justify-center mt-4">
            <a href="/path_to_your_cv.pdf" download class="bg-white text-black py-3 px-6 rounded-lg shadow hover:bg-gray-200 transition duration-300">
                Download my resume
            </a>
        </div>
    </section>
</main>