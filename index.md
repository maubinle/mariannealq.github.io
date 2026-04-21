---
layout: default
---

<div class="profile-section">
    <div class="profile-text">
        <p>I am a postdoctoral fellow at Princeton's Center for Information Technology Policy, working with Manoel Horta Ribeiro and Andy Guess as part of the <a href="https://humans-and-machines.github.io">Humans and Machines lab</a>.</p>
        
        <p>My work traces how AI and other emerging technologies impact online news and civic information consumption. My aim is to help keep the public informed and civically engaged in an accessible, transparent, and equitable way.</p>
        
        <p>I leverage mixed-method techniques from Human-Computer Interaction, Communication, and Computational Social Science to publish in venues like CHI, CSCW, and ICWSM. My work has received a Top Paper award at the International Communication Association.</p>

        <p>I enjoy industry collaborations and did research internships at Reddit, Bell Labs, and Mozilla. I received my PhD from Cornell in Information Science in 2025, where I was in the <a href="https://s.tech.cornell.edu">Social Technologies lab</a>. </p>

    </div>
    
    <div class="profile-sidebar">
        <img src="/assets/img/profile.jpg" alt="{{ site.name }}" class="profile-image">
        <p class="role">Postdoctoral Fellow<br>Princeton Center for Information Technology Policy<br><a href="mailto:{{ site.email }}">{{ site.email }}</a></p>
        
        <div class="social-links">
            {% if site.scholar_url %}
            <a href="{{ site.scholar_url }}" aria-label="Google Scholar"><i class="ai ai-google-scholar"></i></a>
            {% endif %}
            {% if site.bluesky_username %}
            <a href="https://bsky.app/profile/{{ site.bluesky_username }}" aria-label="Bluesky"><i class="fa-brands fa-bluesky"></i></a>
            {% endif %}
            {% if site.linkedin_username %}
            <a href="https://linkedin.com/in/{{ site.linkedin_username }}" aria-label="LinkedIn"><i class="fa-brands fa-linkedin"></i></a>
            {% endif %}
            {% if site.github_username %}
            <a href="https://github.com/{{ site.github_username }}" aria-label="GitHub"><i class="fa-brands fa-github"></i></a>
            {% endif %}
        </div>
    </div>
</div>

## Recent News

<div id="news-list">

<div class="news-item">
    <span class="news-date">July 2026</span>
    <div class="news-content">I will be attending IC2S2 in Vermont, where I am thrilled to be presenting a parallel talk and a plenary lightning talk!</div>
</div>

<div class="news-item">
    <span class="news-date">April 2026</span>
    <div class="news-content">I will be giving a <a href="https://www.networkscienceinstitute.org/talks/marianne-aubin-le-quere">talk at Northeastern University's Network Science Institute</a> on Wednesday, April 29th.</div>
</div>

<div class="news-item">
    <span class="news-date">April 2026</span>
    <div class="news-content">I attended CHI 2026 in Barcelona to present two papers and coordinate a workshop.</div>
</div>

<div class="news-item">
    <span class="news-date">April 2026</span>
    <div class="news-content">I gave a talk at CITP on "Aligning Epistemic Processes and Audience Perceptions for News Consumption." <a href="https://www.youtube.com/watch?v=S6QeVdWyDJE">Watch it on YouTube.</a></div>
</div>

<div class="news-item">
    <span class="news-date">August 2025</span>
    <div class="news-content">I started my new role as a Postdoctoral Research Fellow at Princeton's Center for Information Technology Policy.</div>
</div>

<div class="news-item">
    <span class="news-date">July 2025</span>
    <div class="news-content">I defended my dissertation, "How AI and Emerging Technologies Impact Local Civic Information Ecosystems." Call me Dr!</div>
</div>

<div class="news-item">
    <span class="news-date">May 2025</span>
    <div class="news-content">Attended CHI 2025 in Yokohama, Japan to present paper on LLMs for qualitative research tasks.</div>
</div>

</div>

<p id="news-toggle" style="margin-top: 8px;">
  <a href="#" id="news-toggle-btn" onclick="toggleNews(event)">Show all news ↓</a>
</p>

<script>
(function() {
  var VISIBLE = 5;
  var items = document.querySelectorAll('#news-list .news-item');
  items.forEach(function(el, i) {
    if (i >= VISIBLE) el.style.display = 'none';
  });
  if (items.length <= VISIBLE) {
    document.getElementById('news-toggle').style.display = 'none';
  }
})();

function toggleNews(e) {
  e.preventDefault();
  var items = document.querySelectorAll('#news-list .news-item');
  var btn = document.getElementById('news-toggle-btn');
  var hidden = items[5] && items[5].style.display === 'none';
  items.forEach(function(el, i) {
    if (i >= 5) el.style.display = hidden ? '' : 'none';
  });
  btn.textContent = hidden ? 'Show fewer ↑' : 'Show all news ↓';
}
</script>

## Selected Publications

{% assign featured = site.publications | where: "featured", true | sort: "year" | reverse %}
{% for pub in featured %}
{% include publication-card.html pub=pub %}
{% endfor %}

<p><a href="/publications/">→ View all publications</a></p>