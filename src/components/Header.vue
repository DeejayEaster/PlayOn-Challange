<template>
  <header id="header-dark">
    <nav
      id="nav-dark"
      class=""
    >
      <div class="primary-nav-container">
        <div class="nav-left"><a
            href="/"
            title="NFHS Network Home"
            class="logo nuxt-link-exact-active nuxt-link-active"
          ><img
              src="../assets/playonLogo.svg"
              alt="NFHS logo"
            ></a><a
            href="/watch-events"
            name="watch events"
            class="main-nav watch-events"
          >
            Watch Events
            <span class="live-events">
              586 Live
            </span></a>
          <div
            id="nav-browse"
            class="main-nav browse"
          >Browse <span class="arrow"></span></div>
          <div
            ontouchstart=""
            class="search-wrapper"
          >
            <form
              action="/search"
              method="get"
              class="nav-search"
            ><label
                for="search"
                class="sr-hidden"
              >Search by typing your school, event, association</label> <input
                id="search"
                name="query"
                type="text"
                placeholder="Find your school, event, association..."
                autocomplete="off"
                value=""
              >
              <div class="search-icon"></div>
              <ul
                class="type-ahead"
                style="display:none;"
              >
                <li class="search-divider"></li>
                <li class="see-all-results">
                  <div
                    type="button"
                    role="button"
                    tabindex="0"
                    class="base-button keyboard-enter"
                    data-v-6c22da06=""
                  >
                    <div
                      tabindex="-1"
                      class="mouse-click"
                      data-v-6c22da06=""
                    >
                      See all results for ""
                    </div>
                  </div>
                </li>
              </ul>
            </form>
            <!---->
          </div>
        </div>
        <div class="nav-right"><a
            href="/subscribe/retail"
            name="subscribe"
            class="main-nav subscribe subscribe-now"
          >Subscribe Now</a>
          <div
            class="notifications-wrap"
            style="display:none;"
            data-v-226a7cd0=""
          >
            <div
              type="button"
              role="button"
              tabindex="0"
              class="base-button keyboard-enter nav-account"
              data-v-6c22da06=""
              data-v-226a7cd0=""
            >
              <div
                tabindex="-1"
                class="mouse-click"
                data-v-6c22da06=""
              ><img
                  src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyMCIgaGVpZ2h0PSIyMCIgdmlld0JveD0iMCAwIDIwIDIwIj4KICAgIDxwYXRoIGZpbGw9IiNGRkYiIGZpbGwtcnVsZT0iZXZlbm9kZCIgZD0iTTkuNjY3IDBjLS44MjggMC0xLjUuNjcyLTEuNSAxLjV2LjY5NWMtMi41ODcuNjY3LTQuNSAzLjAxLTQuNSA1LjgwNXY2bC0yIDJ2MWg2LjI3Yy0uMTc3LjMwNC0uMjcuNjQ5LS4yNyAxIDAgMS4xMDUuODk1IDIgMiAyIDEuMTA0IDAgMi0uODk1IDItMi0uMDAxLS4zNTEtLjA5NS0uNjk2LS4yNzItMWg2LjI3MnYtMWwtMi0yVjhjMC0yLjc5NS0xLjkxNC01LjEzOC00LjUtNS44MDVWMS41YzAtLjgyOC0uNjcyLTEuNS0xLjUtMS41em0wIDRjMi4yMDYgMCA0IDEuNzk0IDQgNHY2LjgyOGwuMTcyLjE3Mkg1LjQ5NWwuMTcyLS4xNzJWOGMwLTIuMjA2IDEuNzk0LTQgNC00eiIvPgo8L3N2Zz4K"
                  alt="Account Icon"
                  class="account-icon"
                  data-v-6c22da06=""
                  data-v-226a7cd0=""
                >
                <!---->
              </div>
            </div>
            <div
              class="closed"
              data-v-5786224b=""
              data-v-226a7cd0=""
            >
              <div
                class="notifications-panel"
                data-v-5786224b=""
              >
                <!---->
              </div>
              <div
                class="page-overlay"
                data-v-5786224b=""
              ></div>
            </div>
          </div>
          <div class="nav-account">
            <div><img
                src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyMCIgaGVpZ2h0PSIyMCIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxwYXRoIGZpbGw9IiNGRkYiIGZpbGwtcnVsZT0iZXZlbm9kZCIgZD0iTTEyIDBDNS4zNzIgMCAwIDUuMzcyIDAgMTJzNS4zNzIgMTIgMTIgMTIgMTItNS4zNzIgMTItMTJTMTguNjI4IDAgMTIgMHptOC4zMzkgMTcuNTIyYTcuMSA3LjEgMCAwIDAtLjM2NC0uNTc4QzE4LjYzIDE0Ljk4OCAxNC4zNDUgMTQgMTIgMTRjLTIuMzQ1IDAtNi42NTUgMS4wNDQtOCAzYTQuMjE4IDQuMjE4IDAgMCAwLS4zMjIuNTQ3QTkuOTU0IDkuOTU0IDAgMCAxIDIgMTJDMiA2LjQ3NyA2LjQ3NyAyIDEyIDJzMTAgNC40NzcgMTAgMTBjMCAyLjA0MS0uNjExIDMuOTQtMS42NjEgNS41MjJ6TTEyIDMuM2EzLjkgMy45IDAgMSAxIDAgNy44IDMuOSAzLjkgMCAwIDEgMC03Ljh6Ii8+Cjwvc3ZnPgo="
                alt="Account Icon"
                class="account-icon"
              ></div>
          </div>
        </div>
      </div>
      <div class="secondary-nav-container"><a
          href="/subscribe/retail"
          class="secondary-nav subscribe"
        >Subscribe</a> <a
          href="/customer-support"
          class="secondary-nav support"
        >Support</a></div>
    </nav>
    <div
      id="account-menu"
      class="account-menu"
      style="display:none;"
    >
      <ul class="account-list">
        <li class="account-greeting">
          Welcome! </li>
        <li class="account-list-item"><a
            href="/member/account"
            class="account-list-link"
          >
            My Account
          </a></li>
        <li class="account-list-item"><a
            href="/member/account#following"
            class="account-list-link"
          >
            Following
            <!---->
          </a></li>
        <li class="account-list-item"><a
            href="/#watch-list"
            class="account-list-link watch-later"
          >
            Watch List
            <!---->
          </a></li>
        <li class="account-list-item"><a
            href="/subscribe/retail"
            class="account-list-link"
          >
            Subscribe
          </a></li>
        <li class="account-list-item"><a
            href="#"
            class="account-list-link logout"
          >
            Log Out
          </a></li>
      </ul>
    </div>
    <div
      class="browse-container"
      style="display:none;"
      data-v-73f51c04=""
    >
      <div
        class="browse-options"
        data-v-73f51c04=""
      >
        <div
          class="browse-top"
          data-v-73f51c04=""
        >
          <div
            type="button"
            role="button"
            tabindex="0"
            class="base-button keyboard-enter close-button"
            data-v-6c22da06=""
            data-v-73f51c04=""
          >
            <div
              tabindex="-1"
              class="mouse-click"
              data-v-6c22da06=""
            ></div>
          </div>
          <div
            type="button"
            role="button"
            tabindex="-1"
            class="base-button keyboard-enter back-arrow-wrapper"
            data-v-6c22da06=""
            data-v-73f51c04=""
          >
            <div
              tabindex="-1"
              class="mouse-click"
              data-v-6c22da06=""
            >
              <!---->
              <div
                class="header"
                data-v-73f51c04=""
                data-v-6c22da06=""
              >
                <p data-v-73f51c04="">Browse</p>
              </div>
            </div>
          </div>
        </div>
        <div
          class="fade-top"
          data-v-73f51c04=""
        ></div>
        <div
          id="browse-page"
          class="browse-page"
          data-v-73f51c04=""
        >
          <div
            class="browse-list"
            data-v-73f51c04=""
          >
            <div
              data-v-73f51c04=""
              class="option-container"
            >
              <div
                data-v-73f51c04=""
                id="first-browse-option"
                tabindex="0"
                role="button"
                action="function () { [native code] }"
                class="browse-option option-button"
              ><span
                  data-v-73f51c04=""
                  class="option-name"
                >Browse by Sport</span> <span
                  data-v-73f51c04=""
                  class="arrow"
                ></span></div>
              <!---->
            </div>
            <div
              data-v-73f51c04=""
              class="option-container"
            >
              <div
                data-v-73f51c04=""
                id=""
                tabindex="0"
                role="button"
                action="function () { [native code] }"
                class="browse-option option-button"
              ><span
                  data-v-73f51c04=""
                  class="option-name"
                >Browse by State</span> <span
                  data-v-73f51c04=""
                  class="arrow"
                ></span></div>
              <!---->
            </div>
            <div
              data-v-73f51c04=""
              class="option-container"
            >
              <div
                data-v-73f51c04=""
                id=""
                tabindex="0"
                role="button"
                action="function () { [native code] }"
                class="browse-option option-button"
              ><span
                  data-v-73f51c04=""
                  class="option-name"
                >Browse by Playoff Events</span> <span
                  data-v-73f51c04=""
                  class="arrow"
                ></span></div>
              <!---->
            </div>
            <div
              data-v-73f51c04=""
              class="option-container"
            >
              <!----> <a
                data-v-73f51c04=""
                href="/find-school"
                class="browse-link"
              >
                <div
                  data-v-73f51c04=""
                  class="browse-option option-button"
                ><span
                    data-v-73f51c04=""
                    class="option-name"
                  >Find Your School</span></div>
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div
      class="browse-overlay"
      style="display:none;"
    ></div>
    <div id="extole-global_header-component"></div>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style scoped>
header {
  width: 100%;
  height: 100px;
  color: #fff;
  font-size: 22px;
  padding: 0 12px;
  background-color: #05243f;
  font-family: 'Montserrat', sans-serif;
}

img {
    height: 62px;
    width: 45px;
    margin: 0 15px
}

.primary-nav-container {
    display: flex;
}

.nav-left {
    flex-grow: 100;
    display: flex;
    align-items: baseline;
}

#header-dark #nav-dark .main-nav {
    margin:10px 24px 0 16px;
    margin-top: 10px;
    font-size: 16px;
    text-transform: capitalize;
    font-weight: 500;
    font-style: normal;
    font-stretch: normal;
    line-height: normal;
    letter-spacing: normal;
    color: #fff;
    position: relative;
}
.sr-hidden{
    display: none;
}
.browse {
    font-weight: 800;
}

#search {
        display: inline-block;
    padding: 5px 0 7px;
    margin: 0;
    background-color: transparent;
    height: 18px;
    width: 100%;
    color: #fff;
    font-family: Montserrat,sans-serif;
    font-weight: 500;
    font-size: 16px;
    border-radius: 0;
    border: none;
    border-bottom: 1px solid #0e75d2;
    width: 250%;
}

span.live-events {
    background-color: red;
    border-radius: 2px;
    font-size: 12px;
    font-weight: 800;
    padding: 2px 4px;
}

.subscribe {
    position: relative;
    right: 40px;
}

.secondary-nav-container {
    display: none;
}

a{
    text-decoration: none;
    color: white;
    font-family: 'Montserrat', sans-serif;
}
</style>