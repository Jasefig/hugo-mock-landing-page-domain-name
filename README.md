# Hugo-Mock-Landing Page

This is hoemwork 1 of Upenn CIS 3500 where I make a Hugo mock landing page for product called Mood Melody.

You can see the example landing page by running Hugo Server and opening the given link.

# Mood Melody

MoodMelody Brainwave-Synced Music App: An innovative product that customizes music based on the listener's brain waves to enhance focus, relaxation, or energy levels. Using a hypothetical brainwave detection device that pairs with the user’s smartphone or computer, the MindMeld app analyzes the user’s current mental state and selects music with tempos, keys, and compositions that scientifically match their needs. Whether the user is studying, meditating, or exercising, MindMeld ensures the soundtrack is perfectly in tune with their mental state. The website would showcase the technology, explain the science behind it, offer subscription plans, and feature a demo section where visitors can experience sample music tailored to different brain states.

# Github Workflow

Includes a github workflow that automatically deploys the hugo website
whenever there is a push to the main branch of the repository.

on:
  push:
    branches:
      - main # Set a branch to deploy
This section specifies that the workflow will be triggered whenever there is a push to the main branch of the repository. You can modify the branch name to match your desired branch.

name: 🛠️ Initialize Hugo Environment
uses: peaceiris/actions-hugo@v2.6.0
with:
    hugo-version: "0.123.4"
    extended: true
This step uses the peaceiris/actions-hugo action to set up the Hugo environment with the specified version (0.123.4) and enabling the extended mode (required for certain Hugo features).

name: 🏗️ Compile Hugo Static Files
run: hugo -D --gc --minify

This step runs the hugo command to build the static files for your website. The -D flag tells Hugo to include draft content, --gc enables garbage collection to remove unused cached resources, and --minify minifies the generated HTML, CSS, and JavaScript files.
