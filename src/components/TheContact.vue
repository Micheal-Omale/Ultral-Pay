<template>
    <section id="contact">
        <div class="container py-20">
            <div class="text-center mb-20">
                <h4 class="font-bold text-color-secondary mb-4">Got A Question</h4>
                <h1 class="title capitalize">Get in touch</h1>
            </div>
            
            <form action="submit">
                <div class="w-full m-auto text-center md:w-2/3">
                    <div class="grid gap-5 md:grid-cols-2 mb-5 bg-color-primary-dark">
                        <input class="bg-gray-300 w-full p-3 rounded-lg  border border-gray-400 text-color-primary-dark focus:bg-color-secondary focus:outline-none text-sm block" type="text" placeholder="Name">
                        <input class="bg-gray-300 w-full p-3 rounded-lg  border border-gray-400 text-color-primary-dark focus:bg-color-secondary focus:outline-none text-sm block" type="email" placeholder="Email">
                        <input class="bg-gray-300 w-full p-3 rounded-lg  border border-gray-400 text-color-primary-dark focus:bg-color-secondary focus:outline-none text-sm block" type="tel" placeholder="Phone">
                        <input class="bg-gray-300 w-full p-3 rounded-lg  border border-gray-400 text-color-primary-dark focus:bg-color-secondary focus:outline-none text-sm block" type="text" placeholder="Company">
                    </div>
    
                    <textarea class="w-full rounded-lg text-color-primary-dark p-3 focus:bg-color-secondary focus:text-white border focus:outline-none bg-gray-300 border-gray-400" name="" id="" cols="30" rows="10" placeholder="Message"></textarea>
    
                    <button class="btn mt-10">Send Message</button>
                </div>
            </form>
        </div>
     </section>
</template>