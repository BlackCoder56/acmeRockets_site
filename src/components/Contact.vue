<template>
    <h2 class="text-4xl font-bold text-center sm:text-5xl mb-6 text-slate-900 dark:text-white">
        Contact Us
    </h2>
    <form action="" class="max-w-4xl mx-auto text-2xl sm:text-3xl flex flex-col items-left gap-4">
        <label for="subject" >Subject:</label>
        <input type="text" id="subject" name="subject" required minlength="3" maxlength="60" placeholder="Your Subject"
        class="w-full text-black  sm:text-3xl p-3 rounded-xl border border-solid border-slate-900 dark:bg-white dark:border-none " />
        <label for="message">Message:</label>
        <textarea name="message" id="message" cols="30" rows="10" placeholder="Your Message" required class="w-full text-black  sm:text-3xl p-3 rounded-xl border border-solid border-slate-900 dark:border-none  dark:bg-white" ></textarea>
        <button class="bg-teal-700 hover:bg-teal-600 active:bg-teal- text-white p-3 w-48 rounded-xl border border-solid border-slate-900 dark:border-none">Submit</button>
    </form>
</template>