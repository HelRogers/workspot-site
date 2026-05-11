---
layout: layouts/base.njk
title: Contact
permalink: /contact/
description: Get in touch with Helenor Rogers at WorkSpot Ltd.
---

<section class="hero">
  <div class="container">
    <span class="eyebrow">Contact</span>
    <h1>Say hello<span class="accent" aria-hidden="true"></span></h1>
    <p class="lede" style="margin-top: 2rem; max-width: 56ch;">The quickest way to reach Helenor is by email or LinkedIn. If you would rather use the form below, it lands in the same inbox.</p>
  </div>
</section>

<section style="border-top: 1px solid var(--rule);">
  <div class="container two-col">
    <h2>Get in touch</h2>
    <div>
      <div class="prose" style="margin-bottom: 2.5rem;">
        <p>
          <strong>Email</strong><br>
          <a href="mailto:{{ site.email }}">{{ site.email }}</a>
        </p>
        <p>
          <strong>LinkedIn</strong><br>
          <a href="{{ site.social.linkedin }}" target="_blank" rel="noopener">Connect with Helenor Rogers</a>
        </p>
      </div>

      <form name="contact" method="POST" action="/thanks/" data-netlify="true" netlify-honeypot="bot-field" class="form">
        <input type="hidden" name="form-name" value="contact">
        <p hidden>
          <label>Do not fill this out: <input name="bot-field"></label>
        </p>

        <div>
          <label for="name">Your name</label>
          <input type="text" id="name" name="name" required>
        </div>
        <div>
          <label for="email">Email</label>
          <input type="email" id="email" name="email" required>
        </div>
        <div>
          <label for="message">Message</label>
          <textarea id="message" name="message" rows="5" required></textarea>
        </div>
        <div>
          <button type="submit" class="btn">Send message →</button>
        </div>
      </form>
    </div>
  </div>
</section>
