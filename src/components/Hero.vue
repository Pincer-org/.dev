<script setup>
  import BlueButton from './buttons/BlueButton.vue'
  import GhButton from './buttons/GhButton.vue'
</script>
<template>
  <div class="hero">
    <div class="left">
      <h1>Welcome to Pincer!</h1>

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

      <h2>Want to explore Pincer?</h2>

      <nav>
        <ul>
          <li>
            <svg width="24" height="24" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
              <g fill="black">
                <path d="M12 0C5.37 0 0 5.37 0 12C0 17.31 3.435 21.795 8.205 23.385C8.805 23.49 9.03 23.13 9.03 22.815C9.03 22.53 9.015 21.585 9.015 20.58C6 21.135 5.22 19.845 4.98 19.17C4.845 18.825 4.26 17.76 3.75 17.475C3.33 17.25 2.73 16.695 3.735 16.68C4.68 16.665 5.355 17.55 5.58 17.91C6.66 19.725 8.385 19.215 9.075 18.9C9.18 18.12 9.495 17.595 9.84 17.295C7.17 16.995 4.38 15.96 4.38 11.37C4.38 10.065 4.845 8.985 5.61 8.145C5.49 7.845 5.07 6.615 5.73 4.965C5.73 4.965 6.735 4.65 9.03 6.195C9.99 5.925 11.01 5.79 12.03 5.79C13.05 5.79 14.07 5.925 15.03 6.195C17.325 4.635 18.33 4.965 18.33 4.965C18.99 6.615 18.57 7.845 18.45 8.145C19.215 8.985 19.68 10.05 19.68 11.37C19.68 15.975 16.875 16.995 14.205 17.295C14.64 17.67 15.015 18.39 15.015 19.515C15.015 21.12 15 22.41 15 22.815C15 23.13 15.225 23.505 15.825 23.385C18.2072 22.5807 20.2772 21.0497 21.7437 19.0074C23.2101 16.965 23.9993 14.5143 24 12C24 5.37 18.63 0 12 0Z"/>
              </g>
            </svg>
            <a href="https://github.com/pincer-org/pincer">Take o look at the GitHub repository</a>

          </li>
          <li>
            <svg width="24" height="24" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
              <g fill="black">
                <path d="M20.3173 4.36032C18.761 3.64612 17.1189 3.13638 15.4318 2.84382C15.4165 2.84124 15.4008 2.84346 15.3868 2.85018C15.3728 2.85689 15.3613 2.86777 15.3538 2.88132C15.1423 3.25632 14.9083 3.74682 14.7448 4.13082C12.9262 3.85483 11.0764 3.85483 9.25776 4.13082C9.07538 3.70305 8.86906 3.28588 8.63977 2.88132C8.63207 2.86792 8.6205 2.85717 8.60658 2.85047C8.59265 2.84378 8.57703 2.84146 8.56177 2.84382C6.87427 3.13482 5.23176 3.64482 3.67626 4.36032C3.66295 4.3654 3.65182 4.37494 3.64477 4.38732C0.533765 9.03581 -0.319735 13.5703 0.0987651 18.0478C0.100265 18.0688 0.113765 18.0898 0.130265 18.1033C1.94185 19.4452 3.96815 20.4698 6.12276 21.1333C6.13798 21.1381 6.15432 21.1379 6.16943 21.1328C6.18454 21.1277 6.19761 21.1179 6.20676 21.1048C6.66876 20.4748 7.07976 19.8103 7.43376 19.1113C7.44114 19.0969 7.44367 19.0805 7.44097 19.0646C7.43826 19.0486 7.43048 19.034 7.41877 19.0228C7.41101 19.0155 7.40182 19.0099 7.39176 19.0063C6.74551 18.7579 6.11961 18.4595 5.51977 18.1138C5.50301 18.1043 5.49055 18.0887 5.48497 18.0703C5.47938 18.0519 5.4811 18.032 5.48977 18.0148C5.49487 18.0036 5.50259 17.9939 5.51226 17.9863C5.63826 17.8918 5.76427 17.7928 5.88427 17.6938C5.89487 17.6853 5.90758 17.6798 5.92106 17.678C5.93454 17.6761 5.94826 17.678 5.96076 17.6833C9.88926 19.4773 14.1418 19.4773 18.0223 17.6833C18.0352 17.6777 18.0495 17.6757 18.0635 17.6776C18.0775 17.6794 18.0907 17.685 18.1018 17.6938C18.2218 17.7928 18.3478 17.8918 18.4738 17.9863C18.484 17.9938 18.4922 18.0037 18.4976 18.0151C18.5031 18.0265 18.5056 18.039 18.505 18.0517C18.5045 18.0643 18.5007 18.0766 18.4942 18.0874C18.4877 18.0983 18.4786 18.1073 18.4678 18.1138C17.8693 18.4627 17.2426 18.7608 16.5943 19.0048C16.5839 19.0086 16.5745 19.0145 16.5668 19.0223C16.559 19.0301 16.553 19.0395 16.5493 19.0498C16.5458 19.0598 16.5444 19.0705 16.5452 19.081C16.546 19.0916 16.5489 19.1019 16.5538 19.1113C16.9138 19.8088 17.3263 20.4748 17.7793 21.1048C17.7884 21.1179 17.8015 21.1277 17.8166 21.1328C17.8317 21.1379 17.8481 21.1381 17.8633 21.1333C20.0215 20.4719 22.0511 19.4472 23.8648 18.1033C23.8738 18.097 23.8814 18.0888 23.8869 18.0792C23.8923 18.0696 23.8955 18.0588 23.8963 18.0478C24.3973 12.8713 23.0578 8.37432 20.3473 4.38882C20.3445 4.38223 20.3405 4.37629 20.3353 4.37139C20.3301 4.36648 20.324 4.36271 20.3173 4.36032V4.36032ZM8.02027 15.3208C6.83677 15.3208 5.86326 14.2348 5.86326 12.9028C5.86326 11.5693 6.81877 10.4833 8.02027 10.4833C9.23077 10.4833 10.1953 11.5783 10.1773 12.9028C10.1773 14.2348 9.22177 15.3208 8.02027 15.3208ZM15.9943 15.3208C14.8123 15.3208 13.8373 14.2348 13.8373 12.9028C13.8373 11.5693 14.7928 10.4833 15.9943 10.4833C17.2048 10.4833 18.1708 11.5783 18.1513 12.9028C18.1513 14.2348 17.2048 15.3208 15.9943 15.3208Z"/>
              </g>
            </svg>
            <a href="https://discord/pincer">Join our Discord community</a>
          </li>
          <li>
            <svg width="24" height="24" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
              <g fill="black">
                <path d="M23.922 13.5778V17.4921L20.5507 18.7191L20.4728 18.7731L20.523 18.8121L23.973 17.5551L24 17.5198V13.5231L23.9453 13.4878L23.922 13.5778ZM23.6213 5.61658L20.5823 6.72658V10.6363L23.922 9.42133V5.50708L23.6213 5.61658ZM23.922 13.4571V9.54283L20.586 10.7578V14.6721L23.922 13.4571ZM20.469 14.7111V10.8013L17.172 12.0006V15.9148L20.469 14.7111ZM17.0347 19.9956V16.0858L13.7228 17.2888V21.2031L17.0347 19.9956ZM17.172 16.0588V19.9258L20.484 18.7191V14.8521L17.172 16.0551V16.0588ZM19.2623 17.9376C18.8955 18.0733 18.6022 17.8626 18.6022 17.4763C18.6022 17.0856 18.8955 16.6596 19.2623 16.5261C19.629 16.3941 19.926 16.6041 19.926 16.9911C19.926 17.3818 19.629 17.8078 19.2623 17.9368V17.9376ZM13.227 9.31558L13.59 9.18358L10.305 7.98358L6.98025 9.19483L7.086 9.23383L10.2697 10.3948L13.227 9.31558ZM20.508 10.6641V6.74983L17.172 7.96483V11.8791L20.508 10.6641ZM17.0588 11.9181V8.00383L13.758 9.20683V13.1166L17.0588 11.9181ZM13.6448 9.24583L10.3087 10.4608V14.3751L13.6448 13.1601V9.24583ZM6.906 13.1638L10.23 14.3751V10.4608L6.906 9.25408V13.1638ZM10.3402 7.87108L13.6215 9.06583V5.19883L10.3402 4.00408V7.87108ZM20.508 2.71483L17.1907 3.92158V7.83583L20.508 6.62908V2.71483ZM16.9493 3.90208L13.7235 2.72983L10.4535 3.92158L13.6807 5.09383L16.9493 3.90208ZM15.363 4.60483L13.7422 5.19883V9.06583L17.0595 7.85908V3.99208L15.363 4.60483ZM14.973 7.38283C14.6048 7.52008 14.3123 7.30858 14.3123 6.92158C14.3123 6.53083 14.6055 6.10483 14.973 5.97283C15.3398 5.84008 15.6368 6.04708 15.6368 6.43783C15.6368 6.82783 15.3398 7.25008 14.973 7.38283ZM10.23 18.4101V14.4958L6.906 13.2846V17.1988L10.23 18.4101ZM13.68 17.1838V13.2696L10.3087 14.4958V18.4101L13.68 17.1838ZM13.758 17.1516L17.055 15.9523V12.0381L13.758 13.2373V17.1516ZM13.68 21.2188L10.3087 22.4451V18.5308H10.23V22.4451L6.906 21.2338V17.3196L6.855 17.2656L6.828 17.2026L3.492 15.9913V12.0463L3.52725 12.0583L6.81225 13.2531L6.828 13.1751L3.56625 11.9871L6.828 10.8043V10.6941L3.57 9.50683L6.828 8.31883V9.19408L6.906 9.14008V6.76933L10.164 7.95208L10.2232 7.89433L7.086 6.74908L6.98025 6.71383L10.2232 5.53408V5.44783L6.855 6.67483V6.69358L6.828 6.71383V8.23258L3.441 9.46783V9.48658L3.414 9.50683V13.5148L0.02325 14.7448V14.7651L0 14.7838V18.7761L0.02325 18.8151L3.426 20.0541L3.43425 20.0458L3.441 20.0578L6.84 21.2961L6.84825 21.2878L6.855 21.2998L10.254 22.5336L10.2697 22.5253L10.281 22.5336L13.7302 21.2796L13.758 21.2406L13.68 21.2188ZM3.492 9.56158L6.75 10.7458L3.492 11.9338V9.56158ZM3.39825 19.9611L0.078 18.7543V14.8401L3.39825 16.0468V19.9611ZM3.414 15.9688L0.15225 14.7846L3.414 13.5973V15.9726V15.9688ZM6.81225 21.1986L3.492 19.9918V16.0776L6.81225 17.2888V21.1986ZM23.7892 5.43358L20.5823 4.26583V6.60208L23.7892 5.43358ZM20.3873 2.64508L17.148 1.46533L13.8787 2.65258L17.1248 3.83683L20.3873 2.64508Z"/>
              </g>
            </svg>
            <a href="https://pypi.org/project/Pincer">Download the PyPI package</a>
          </li>
          <li>
            <svg width="24" height="24" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
              <g fill="black">
                <path d="M4.76564 18.75H21.75V0.75H4.71877C3.9653 0.752423 3.24338 1.05281 2.7106 1.5856C2.17781 2.11838 1.87742 2.8403 1.875 3.59377V20.168H1.87552C1.87552 20.175 1.875 20.182 1.875 20.1892C1.875 21.8486 3.17728 23.2501 4.71877 23.2501H21.75V21.75H4.71877C4.0155 21.75 3.375 21.006 3.375 20.1891C3.375 19.4091 4.0118 18.75 4.76564 18.75ZM16.875 2.26561V10.3664L14.6063 8.37464L12.375 10.3547V2.26561H16.875ZM10.875 2.25V12.375H12.3582L14.6117 10.3754L16.8893 12.375H18.375V2.25H20.25V17.25H6.37875L6.375 2.25H10.875ZM4.71877 2.25H4.875L4.87856 17.25H4.76545C4.27771 17.2501 3.79844 17.3775 3.375 17.6195V3.60548C3.37385 3.24766 3.51469 2.904 3.7666 2.64989C4.01852 2.39577 4.36095 2.25196 4.71877 2.25V2.25Z"/>
              </g>
            </svg>
            <a href="https://docs.pincer.dev">Get Started with the documentation</a>
          </li>
        </ul>
      </nav>
    </div>
    <div class="right">
      <img src="img/window_code_block.png"
           alt="API simple Discord bottom with a /say command written written using pincer."/>
      <img src="img/discord_command_demo.png" alt="An user writing and triggering the /say example command.">
      <img src="img/command_output.png" alt="The result of the /say command.">
    </div>
  </div>
</template>

<style lang="scss" scoped>
  h1 {
    font-size: 1.75rem;
  }

  h2, p {
    margin-top: 2rem;
  }

  p {
    text-align: justify;
  }

  .github-buttons {
    display: flex;
    flex-flow: row wrap;
    gap: 10px;
  }

  ul {
    li {
      svg g {
        fill: var(--text-color);
      }

      gap: 10px;
      display: flex;
      align-items: center;
      list-style: none;
      margin: 10px 0;

      &:hover, a:focus {
        outline: 0;
        text-decoration: underline;
      }
    }

    padding-left: 0;
    display: grid;
    gap: 5px;
  }

  .right {
    display: grid;
    gap: 20px;

    img {
      width: calc(100vw - 40px);
    }
  }
</style>
