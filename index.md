---
layout: page
title: The Timeline
width: small
---

<p>This is the master timeline with a quick add above, a <a href="javascript:void(window.open('https://github.com/kinlane/timeline/issues/new?labels=timeline&title=%27+encodeURIComponent(document.title)+%27&body=%27+getSelection().toString()+%27%20~%20%27+encodeURIComponent(location.href)));">Timeline</a> bookmarklet you can drag to your toolbar, or you can checkout the repo and add to the <a href="https://github.com/kinlane/timeline/blob/main/_data/timeline.yml" target="_blank">timeline.yml</a>.</p>
<div class="tm-timeline uk-margin-large-top">
    {% for version in site.data.timeline %}
    <div class="tm-timeline-entry">
        <div class="tm-timeline-time">
            <h5>{{ version.date }}</h5>
        </div>
        <div class="tm-timeline-body">
            <h3 class="uk-flex uk-flex-middle" style="font-size: 14px;">{{ version.title }}{% if version.label %}{% for label in version.label %}<span class="uk-label uk-margin-small-left">{{ label }}</span>{% endfor %}{% endif %}</h3>
            <ul class="uk-list">
                {% for item in version.list %}
                <li>{{ item }}</li>
                {% endfor %}
            </ul>
        </div>
    </div>
    {% endfor %}
</div>

