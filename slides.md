---
theme: seriph
background: /holiday-cheer.png
class: text-center
highlighter: shiki
drawings:
  persist: false
transition: slide-left
title: Holiday Cards with Gemini & Firebase
---

# AI-Powered Holiday Cards
### Gemini 3 Flash + Genkit + Firebase

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer hover:bg-white/10" title="Next Page">
    Press Space for next page <carbon:arrow-right class="inline"/>
  </span>
</div>

<div class="absolute bottom-5 left-0 right-0 text-center opacity-60 text-[10px] text-white/80">
  Background image from <a href="https://unsplash.com" target="_blank" class="underline hover:text-white">Unsplash</a>
</div>


---
transition: fade-out
---

# The Concept

Creating a personalized, single-page holiday cards app that leverages the power of Large Language Models to generate unique messages and themes.

- **Personalization**: User provides a few details, AI does the rest.
- **Speed**: Built with **Gemini 3 Flash** for near-instant responses.
- **Modern Stack**: React, Tailwind CSS, and Firebase Genkit.
- **Scalable**: Serverless architecture using Firebase.

---

# The Tech Stack

<div class="grid grid-cols-2 gap-4">
<div>

### The Brain
- **Gemini 3 Flash**: High-speed, lightweight LLM.
- **Nano Banana**: Optimized for specific generative tasks.

### The Bridge
- **Firebase Genkit**: Framework for building & deploying AI features.
- **Firebase Cloud Functions**: Serverless execution.
</div>
<div>

### The Experience
- **React**: Modern component-based UI.
- **Tailwind CSS**: Utility-first styling for beautiful designs.
- **Firestore**: Real-time database for storing cards.
</div>
</div>

---

# Gemini 3 Flash & Nano Banana

<div class="flex flex-col gap-4">

> **Gemini 3 Flash** is designed for speed and efficiency, making it perfect for real-time applications like interactive greeting cards.

- **Multimodal**: Can process text, images, and more.
- **Low Latency**: Faster than Gemini 3 Pro for simple creative tasks.
- **Nano Banana**: Specialized model variants for specific, high-efficiency workflows.

</div>

---

# Firebase Genkit

The modern developer's toolkit for AI.

- **Flows**: Define complex AI logic as typed, testable functions.
- **Plugins**: Easy integration with Gemini, Firestone, and more.
- **Local Dev**: Genkit UI for testing prompts and flows locally.
- **Deployment**: Native support for Firebase Cloud Functions.

```typescript
const holidayCardFlow = defineFlow({
  name: 'holidayCardFlow',
  inputSchema: z.object({ recipient: z.string(), theme: z.string() }),
}, async (input) => {
  const result = await generate({
    model: gemini3Flash,
    prompt: `Write a holiday card for ${input.recipient} with a ${input.theme} theme.`,
  });
  return result.text();
});
```

---

# Backend Architecture

How it all fits together in Firebase.

1. **User Action**: React frontend sends a request to a Genkit-powered Cloud Function.
2. **AI Generation**: Genkit calls Gemini 3 Flash to generate the card content.
3. **Storage**: The generated card and metadata are stored in Firestore.
4. **Delivery**: The app retrieves the card via a unique ID for sharing.

---

# React + Tailwind CSS UI

A premium experience for holiday cheer.

- **Glassmorphism**: Sleek, modern overlays for holiday vibes.
- **Responsive Layout**: Works beautifully on mobile and desktop.
- **Real-time Feedback**: Showing AI progress with tailored loaders.

```html
<div class="bg-white/10 backdrop-blur-md rounded-xl p-8 border border-white/20">
  <h2 class="text-3xl font-bold bg-gradient-to-r from-red-400 to-green-400 bg-clip-text text-transparent">
    Happy Holidays!
  </h2>
  <p class="mt-4 text-gray-200">
    {generatedMessage}
  </p>
</div>
```

---

# Implementation Highlights

1. **Setup**: `firebase init functions` + `genkit init`.
2. **Developing**: Use the Genkit Developer UI to polish prompts.
3. **Connecting**: Call functions from React using `httpsCallable`.
4. **Deploying**: `firebase deploy`.

---

# Conclusion

Combining **Gemini**'s intelligence with **Genkit**'s developer experience and **Firebase**'s scalability allows for creating powerful AI apps in hours, not weeks.

- **Links**:
  - [Slidev Guide](https://sli.dev)
  - [Firebase Genkit](https://genkit.dev)
  - [Google Gemini](https://deepmind.google/models/gemini)

---
layout: end
---

# Thank You!
Questions? Check the [repo](https://github.com/alexastrum/slidev-firebase)!

---

# Under the Hood: AI Generation

Built with intelligence and speed.

- **Antigravity**: The engine behind the rapid development of this project.
- **Gemini 3 Flash**: Leveraging Google's latest high-speed, 1M+ context model.
- **Scalable agentic workflow**: From idea to code to presentation in minutes.

---

# Under the Hood: Sli.dev

Modern scripting for developer presentations.

- **Markdown First**: Content is just Markdown, version-controllable and easy to edit.
- **Vue Integration**: Uses Vue components directly in your slides for interactive demos (not React, but close enough).
- **Developer Experience**: Built-in code highlighting and more.
- **Flexibility**: Complete control over styling with Tailwind CSS and CSS.

---

# Under the Hood: Firebase Hosting

Fast, secure, and free publishing.

- **Firebase CLI**: Deploy with a single command: `firebase deploy`.
- **Instant**: Deployments are fast and predictable.
- **Free Tier**: Host this presentation at no cost, no CC required.
