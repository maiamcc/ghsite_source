---
layout: page
title: "Crosswords By Maia"
sidebar: true
---
I write crossword puzzles sometimes (using <a href="http://beekeeperlabs.com/crossfire/" target="_blank">Crossfire</a>). Take a look, and enjoy! (I'm new at this; feedback is welcome.)

To solve these puzzles on your computer, open the `.puz` file in [this online solver](http://derekslager.com/puz/) or in [Across Lite](https://www.litsoft.com/across/alite/download/).

<div class="puzzle-container">
    {% for puzzle in site.data.crosswords %}
    <div class="puzzle">
        <h3 class="title">
            <a href="/crosswords/{{puzzle.slug}}.html">{{ puzzle.title }}</a>
        </h3>

        <div class="info completed"><em>Completed</em>: {{ puzzle.date }}</div>
        <div class="info notes"><em>Constructor notes</em>: {{ puzzle.notes }}</div>
        <div class="info difficulty"><em>Approx. difficulty</em>: NYT {{ puzzle.day_of_week }}</div>
        <div class="info files"><em>Files</em>:
            <a href="/crosswords/{{puzzle.slug}}/{{puzzle.slug}}.pdf">PDF</a> |
            <a href="/crosswords/{{puzzle.slug}}/{{puzzle.slug}}.png">PNG</a> |
            <a href="/crosswords/{{puzzle.slug}}/{{puzzle.slug}}.puz" download>PUZ</a> |
            <a href="/crosswords/{{puzzle.slug}}/{{puzzle.slug}}.ipuz" download>IPUZ</a> |
            <a href="/crosswords/{{puzzle.slug}}/{{puzzle.slug}}-solution.png">solution</a>
        </div>
    </div>
    {% endfor %}
</div>
