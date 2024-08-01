<script>
    import Step from "./Step.svelte";

    let steps = [
        {name: 'Kumon & RSM', icon: 'fa-solid fa-book'},
        {name: 'Rocklin High School', icon: 'fa-solid fa-school'},
        {name: 'Sierra College', icon: 'fa-solid fa-graduation-cap'}
    ]

    let benefits = [
        {name:'a seasoned tutor', desc: "I am a seasoned tutor with a progressive track record, starting from helping friends and classmates to joining the Rocklin High tutoring center. I further expanded my experience by volunteering 40 hours at Whitney High School as a math tutor, demonstrating my commitment to supporting students' success in mathematics."},
        {name:'a team player', desc: "As a team player, I have played a key role in organizing Mustang Math, a volunteering effort to host math competitions for middle school students. I also served as a team captain for the Berkeley Math Tournament and competed in the Stanford Math Tournament, showcasing my leadership and competitive spirit in mathematics."},
        {name:'a competitor', desc: "I actively compete in various math competitions, including Math League at Rocklin High School, the AMC, and the Rocklin High School Integration Bee. I consistently achieve high marks and was even featured in the RHS magazine for my accomplishments."},
    ]
</script>

<main class="flex flex-col flex-1 p-4">
    <section
        id="introPage"
        class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14"
    >
        <div
            class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10"
        >
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                Hi! I'm <span class="poppins text-violet-400">Aryavrat</span> Mishra
                <br />Math
                <span class="poppins text-violet-400">Tutor</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                My <span class="text-violet-400"> favorite math</span> Geometry, Algebra, Calculus, Combinatorics, and Trigonometry!
            </p>
            <a href="https://calendly.com/aryavratmishra007/tutoring-session" target="_blank"
                class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950"
            >
                <div
                    class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
                />
                <h4 class="relative z-9">Schedule a class &rarr;</h4>
            </a>
        </div>
        <div class="relative shadow-2xl grid place-items-center">
            <img src = {'images/new-profile.png'} alt="Profile image" class="object-cover z-[2] max-h-[70vh] shadow-none transition-shadow duration-300 hover:shadow-lg hover:shadow-gray-400"/>
        </div>
    </section>


    <section id="quals" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-lg sm:text-xl md:text-2xl">My previous math education.
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Want to <span class="poppins text-violet-400">see</span> my qualifications?
            </h3>
        </div>

        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>I received extensive tutoring in mathematics through Kumon and RSM, successfully completing both of their math programs at just 14 years old.
                    While RSM taught me <strong class="text-violet-400">geometry and algebra</strong> in depth, I learned <strong class="text-violet-400">calculus</strong> from Kumon.
                    I qualified for RSM's exclusive NMCP program, where I studied <strong class="text-violet-400">combinatorics and competition math</strong> in depth.</p>
            </Step>

            <Step step={steps[1]}>
                <p>At Rocklin High School, I completed <strong class="text-violet-400">Integrated Math 1, 2, and 3</strong>, along with <strong class="text-violet-400">AP Calculus AB and BC</strong>, finishing the entire math program by my sophomore year. 
                I actively competed in Math League competitions, consistently achieving high scores, and was a dedicated member of the school's math team.
            </p>
            </Step>

            <Step step={steps[2]}>
                <p>
                To further my math education, I enrolled at Sierra College. At the age of 14, I took <strong class="text-violet-400">Trigonometry and Pre-Calculus</strong>, and at 15, I took <strong class="text-violet-400">Calculus 2 (Math 31)</strong>, consistently maintaining an A in these classes. I excelled in challenging topics such as <strong class="text-violet-400">complex numbers and advanced integration techniques</strong>, and occasionally helped my peers understand difficult concepts. Additionally, I joined the math and programming club to extend my passion for math to the collegiate level.
            </p>
            </Step>
        </div>
    </section>


    <section id="about" class="py-20 pt-10 lg:pt-16 flex flex-col gap-16 sm:gap-20 md:gap-24 relative">
        <div class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4">
            <h6 class="text-lg sm:text-xl md:text-2xl">Want to know more?</h6>
            <h3 class="font-semibold text-3xl xm:text-4xl md:text-5xl">A bit <span class="poppins text-violet-400">about</span> me.</h3>
        </div>
        <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">I am . . .</p>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
            {#each benefits as benefit, index}
            <div class="flex gap-6 sm:gap-8">
                <div class="flex gap-6 sm:gap-8">
                    <p class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold">
                        0{index+1}    
                    </p>
                        <div class="flex flex-col gap-6 sm:gap-8">
                            <h3 class="text-2xl xm:text-3xl md:text-5xl">
                                {benefit.name}
                            </h3>
                            <p>{benefit.desc}</p>
                        </div>
                </div>
            </div>
            {/each}
        </div>
        <section>
            <h5 class={" text-2xl sm:text-3xl font-semibold text-center poppins py-4"}>
                The <span class="text-violet-400">Complete</span> Package
            </h5>        
            <div
            class="flex flex-col overflow-x-scroll gap-10 max-w-[800px] mx-auto w-full"
            >
            <table class="bg-white text-slate-700 rounded text-center">
                <thead class={"border-b border-solid border-slate-200  "}>
                    <tr class="">
                        <th />
                        <th class="whitespace-nowrap p-2 px-4">Candidate #1</th>
                        <th class="whitespace-nowrap p-2 px-4">Candidate #2</th>
                        <th class="whitespace-nowrap p-2 px-4">Candidate #3</th>
                        <th
                            class="bg-violet-700 text-white whitespace-nowrap p-4 px-8"
                            >Me</th
                        >
                    </tr>
                </thead>
                <tbody>
                    <tr class="border-b border-solid border-slate-200">
                        <td
                            class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                            >Dedication</td
                        >
                        <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-green-500" /></td>
                    </tr>
                    <tr class="border-b border-solid border-slate-200">
                        <td
                            class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                            >Tutoring Experience</td
                        >
                        <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-green-500" /></td>
                    </tr>
                    <tr>
                        <td
                            class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                            >College Education</td
                        >
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-green-500" /></td>
                    </tr>
                    <tr class="border-t border-solid border-slate-200">
                        <td
                            class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                            >Affordable</td
                        >
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-green-500" /></td>
                    </tr>
                </tbody>
            </table>
        </div>
        <div class="mt-5 text-center mx-auto -mt-12 italic sm:hidden opacity-50">
            <p>Scroll to see more &rarr;</p>
        </div>
        <p class="mx-auto text-center mt-5">So why not invest?</p>

    </section>
</main>
    