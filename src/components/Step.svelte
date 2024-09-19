<script>
    export let step;
</script>

<a href={step.href} target="_blank" class="p-4 sm:p-6 md:p-8 flex flex-col gap-4 rounded-lg border border-solid border-violet-700 text-center group cursor-pointer hover:border-violet-400 hover:shadow-lg transition-all duration-300">
    <!-- Animation d'icône -->
    <div class="bg-slate-50 grid place-items-center px-4 text-5xl md:text-6xl -mt-10 sm:-mt-12 md:-mt-14 lg:-mt-16 mx-auto duration-200 group-hover:scale-110 group-hover:rotate-6 transition-all">
        <i class={step.icon}/>
    </div>
    <h3 class="font-medium text-xl sm:text-2xl md:text-3xl group-hover:text-violet-700 transition-colors duration-300">{step.name}</h3>
    <slot/>
    <div class="flex-1 flex justify-between gap-4 items-center">
        <!-- Animation pour le bouton "Go to" -->
        <div class="ml-auto cursor-pointer relative overflow-hidden">
            <!-- On garde le texte mais on enlève l'animation sur la flèche -->
            <p class="relative z-10">Go to &RightArrow;</p>
            <!-- Le fond blanc glissant reste -->
            <div class="absolute inset-0 bg-white z-0 translate-x-[-100%] group-hover:translate-x-0 transition-transform duration-300"></div>
        </div>
    </div>
</a>
