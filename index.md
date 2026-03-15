---
layout: default
title: Home
---

<section class="portfolio-intro">
  <p class="eyebrow">Aspiring Developer Portfolio</p>
  <h1>문제를 끝까지 해결하는 개발자를 목표로 공부하고 있습니다.</h1>
  <p class="lead">
    안녕하세요. 사용자 경험과 안정적인 백엔드 구현에 관심이 많은 대학생 개발자입니다.
    이 공간에는 제가 공부하며 쌓은 기술, 직접 만든 프로젝트, 그리고 학습 과정을 정리한 글을 담아두었습니다.
  </p>
  <div class="quick-facts">
    <div class="fact-card">
      <strong>관심 분야</strong>
      <span>Backend, Database, Web</span>
    </div>
    <div class="fact-card">
      <strong>학습 태도</strong>
      <span>기초를 탄탄히, 기록은 꾸준히</span>
    </div>
    <div class="fact-card">
      <strong>현재 목표</strong>
      <span>실무형 프로젝트 경험 확장</span>
    </div>
  </div>
</section>

<section class="content-section">
  <div class="section-heading">
    <p class="eyebrow">About Me</p>
    <h2>자기소개</h2>
  </div>
  <div class="panel">
    <p>
      새로운 기술을 빠르게 시도하는 것보다, 왜 그렇게 동작하는지 이해하고 설명할 수 있는 개발자가 되고 싶습니다.
      강의와 교재에서 배운 내용을 그대로 끝내지 않고, 작은 서비스와 실습 프로젝트로 연결해보며 제 것으로 만드는 과정을 중요하게 생각합니다.
    </p>
    <p>
      특히 Java 기반 백엔드, 데이터베이스 설계, Git 협업 흐름에 흥미를 느끼고 있으며,
      앞으로는 API 설계와 배포 경험까지 넓혀가며 신뢰할 수 있는 웹 개발자로 성장하는 것이 목표입니다.
    </p>
  </div>
</section>

<section class="content-section">
  <div class="section-heading">
    <p class="eyebrow">Tech Stack</p>
    <h2>기술 스택</h2>
    <p>현재 학습 중인 기술과 프로젝트에 실제로 적용해본 도구들입니다.</p>
  </div>
  {% for category in site.data.skills %}
    <div class="stack-group">
      <h3>{{ category.category }}</h3>
      <div class="chip-list">
        {% for item in category.items %}
          <span class="chip">{{ item }}</span>
        {% endfor %}
      </div>
    </div>
  {% endfor %}
</section>

<section class="content-section">
  <div class="section-heading">
    <p class="eyebrow">Projects</p>
    <h2>프로젝트</h2>
    <p>기획부터 구현, 회고까지 직접 경험하며 성장한 작업들입니다.</p>
  </div>
  <div class="project-grid">
    {% for project in site.data.projects %}
      <article class="project-card">
        <div class="project-top">
          <p class="project-label">{{ project.type }}</p>
          <h3>{{ project.name }}</h3>
          <p class="project-summary">{{ project.summary }}</p>
        </div>
        <ul class="project-points">
          {% for point in project.points %}
            <li>{{ point }}</li>
          {% endfor %}
        </ul>
        <div class="chip-list compact">
          {% for tech in project.stack %}
            <span class="chip">{{ tech }}</span>
          {% endfor %}
        </div>
        {% if project.link %}
          <p class="project-link"><a href="{{ project.link }}">프로젝트 보러 가기</a></p>
        {% endif %}
      </article>
    {% endfor %}
  </div>
</section>

<section class="content-section">
  <div class="section-heading">
    <p class="eyebrow">Blog Direction</p>
    <h2>기술 블로그에서 다루는 내용</h2>
  </div>
  <div class="blog-grid">
    <article class="panel">
      <h3>문제 해결 기록</h3>
      <p>오류 원인 분석, 해결 과정, 다시 같은 문제를 만났을 때의 체크포인트를 정리합니다.</p>
    </article>
    <article class="panel">
      <h3>학습 정리</h3>
      <p>Java, SQL, 웹 개발 기초처럼 개념 이해가 중요한 주제를 제 언어로 다시 설명합니다.</p>
    </article>
    <article class="panel">
      <h3>프로젝트 회고</h3>
      <p>기능 구현보다 한 단계 더 나아가 설계 선택, 아쉬웠던 점, 다음 개선 방향까지 기록합니다.</p>
    </article>
  </div>
</section>
