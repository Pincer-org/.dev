<script setup>
  import BlueButton from './buttons/BlueButton.vue'
  import GhButton from './buttons/GhButton.vue'
</script>
<template>
  <div class="hero">
    <h1>Welcome to Pincer!</h1>
  </div>

  <div class="github-buttons">
    <GhButton
        href="https://pypi.org/project/Pincer"
        badge-url="https://img.shields.io/badge/dynamic/json?label=downloads&query=%24.total_downloads&url=https%3A%2F%2Fapi.pepy.tech%2Fapi%2Fprojects%2FPincer"
        alt="PyPI - Downloads"
    />
    <GhButton
        href="https://pypi.org/project/Pincer"
        badge-url="https://img.shields.io/pypi/v/Pincer"
        alt="PyPI"
    />
    <GhButton
        href="https://pypi.org/project/Pincer"
        badge-url="https://img.shields.io/pypi/pyversions/Pincer"
        alt="PyPI - Python Version"
    />
    <GhButton
        href="https://scrutinizer-ci.com/g/Pincer-org/pincer/?branch=main"
        badge-url="https://scrutinizer-ci.com/g/Pincer-org/pincer/badges/quality-score.png?b=main"
        alt="Scrutinizer Code Quality"
    />
    <GhButton
        href="https://scrutinizer-ci.com/g/Pincer-org/Pincer/build-status/main"
        badge-url="https://scrutinizer-ci.com/g/Pincer-org/Pincer/badges/build.png?b=main"
        alt="Build Status"
    />
    <GhButton
        href="https://pincer.readthedocs.io/en/latest/?badge=latest"
        badge-url="https://readthedocs.org/projects/pincer/badge/?version=latest"
        alt="Documentation Status"
    />
    <GhButton
        href="https://codecov.io/gh/Pincer-org/Pincer"
        badge-url="https://codecov.io/gh/Pincer-org/Pincer/branch/main/graph/badge.svg?token=T15T34KOQW"
        alt="codecov"
    />
    <GhButton
        href="/"
        badge-url="https://tokei.rs/b1/github/pincer-org/pincer?category=code&path=pincer"
        alt="Lines of code"
    />
    <GhButton
        href="/"
        badge-url="https://img.shields.io/github/repo-size/Pincer-org/Pincer"
        alt="Repo Size"
    />
    <GhButton
        href="/"
        badge-url="https://img.shields.io/github/last-commit/Pincer-org/Pincer"
        alt="GitHub last commit"
    />
    <GhButton
        href="/"
        badge-url="https://img.shields.io/github/commit-activity/m/Pincer-org/Pincer?label=commits"
        alt="GitHub commit activity"
    />
    <GhButton
      href="/"
      badge-url="https://img.shields.io/github/license/Pincer-org/Pince"
      alt="GitHub"
    />
    <GhButton
      href="https://discord.gg/pince"
      badge-url="https://img.shields.io/discord/881531065859190804"
      alt="Discord"
    />
    <GhButton
      href="https://github.com/psf/black"
      badge-url="https://img.shields.io/badge/code%20style-black-000000.svg"
      alt="Code style: black"
    />
  </div>

  <p>
    🚀 The snappy asynchronous discord api wrapper API wrapper written with aiohttp & websockets for anyone in the Python community to build their bot with.
  </p>
  <BlueButton text="Learn more" link="/a"/>
</template>

<style scoped>
  h1 {
    font-size: 1.75rem;
  }

  p {
    text-align: justify;
    margin: 20px 0;
  }

  .github-buttons {
    display: flex;
    flex-flow: row wrap;
    gap: 10px;
  }
</style>
