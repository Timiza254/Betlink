/* =========================================================
   BETLINK — MOCK DATA
   Sample sporting events and users so the prototype can be
   demonstrated without a backend. Replace with real API data
   once BetLink has a server.
   ========================================================= */

const SAMPLE_USERS = [
  { username: "kiptoo_j", name: "Joseph Kiptoo" },
  { username: "wanjiku_m", name: "Mary Wanjiku" },
  { username: "otieno_b", name: "Brian Otieno" },
  { username: "achieng_l", name: "Lilian Achieng" },
];

const SAMPLE_EVENTS = [
  {
    sport: "FOOTBALL",
    matchup: "Gor Mahia vs AFC Leopards",
    date: "Sun, 09 Aug · 3:00 PM",
    selectionFor: "Gor Mahia to win",
    selectionAgainst: "AFC Leopards or draw",
    stake: 1500,
    odds: "1.85",
    creator: "kiptoo_j",
  },
  {
    sport: "FOOTBALL",
    matchup: "Manchester City vs Arsenal",
    date: "Sun, 09 Aug · 6:30 PM",
    selectionFor: "Arsenal to win",
    selectionAgainst: "Man City or draw",
    stake: 2500,
    odds: "2.10",
    creator: "wanjiku_m",
  },
  {
    sport: "RUGBY",
    matchup: "Kenya Simbas vs Uganda Cranes",
    date: "Sat, 08 Aug · 4:00 PM",
    selectionFor: "Simbas to win by 10+",
    selectionAgainst: "Simbas win by <10 or lose",
    stake: 800,
    odds: "1.95",
    creator: "otieno_b",
  },
  {
    sport: "BASKETBALL",
    matchup: "Kenya Morans vs Nigeria D'Tigers",
    date: "Mon, 10 Aug · 7:00 PM",
    selectionFor: "D'Tigers to win",
    selectionAgainst: "Morans to win",
    stake: 1200,
    odds: "1.70",
    creator: "achieng_l",
  },
];

/* =========================================================
   TICKER
   ========================================================= */
function buildTicker() {
  const track = document.getElementById("tickerTrack");
  if (!track) return;

  const items = SAMPLE_EVENTS.map((e) => {
    const direction = Math.random() > 0.5 ? "up" : "down";
    const arrow = direction === "up" ? "▲" : "▼";
    return `
      <span class="ticker-item">
        <span class="tk-event">${e.matchup}</span>
        <span class="tk-${direction}">${arrow} ${e.odds}</span>
      </span>`;
  }).join("");

  // duplicate content once so the CSS scroll loop is seamless
  track.innerHTML = items + items;
}

/* =========================================================
   SPOTLIGHT SLIP (signature element)
   ========================================================= */
function buildSpotlightSlip() {
  const container = document.getElementById("spotlightSlip");
  if (!container) return;

  const e = SAMPLE_EVENTS[0];

  container.innerHTML = `
    <div class="slip-meta">
      <span class="slip-sport">${e.sport}</span>
      <span>${e.date}</span>
    </div>
    <div class="slip-body">
      <div class="slip-side for">
        <div class="slip-side-label">SIDE A</div>
        <div class="slip-side-team">${e.selectionFor}</div>
      </div>
      <div class="slip-vs">VS</div>
      <div class="slip-side against">
        <div class="slip-side-label">SIDE B</div>
        <div class="slip-side-team">${e.selectionAgainst}</div>
      </div>
    </div>
    <div class="slip-stakes">
      <div class="slip-stake-block">
        <span class="slip-stake-value">${e.stake.toLocaleString()} VC</span>
        <span class="slip-stake-label">STAKE PER SIDE</span>
      </div>
      <div class="slip-stake-block">
        <span class="slip-stake-value">${(e.stake * 2 * 0.95).toLocaleString()} VC</span>
        <span class="slip-stake-label">WINNER PAYOUT (5% FEE)</span>
      </div>
    </div>
    <div class="slip-footer">
      <span class="slip-odds">Terms: <b>${e.odds}</b> · Created by <b>@${e.creator}</b></span>
      <a href="markets.html" class="btn btn-primary" style="padding:8px 14px;font-size:13px;">Accept</a>
    </div>
  `;
}

/* =========================================================
   UPCOMING EVENTS LIST
   ========================================================= */
function buildEventList() {
  const list = document.getElementById("eventList");
  if (!list) return;

  list.innerHTML = SAMPLE_EVENTS.slice(0, 3).map((e) => `
    <div class="event-card">
      <div class="event-card-top">
        <span class="event-sport">${e.sport}</span>
        <span class="event-time">${e.date}</span>
      </div>
      <div class="event-matchup">${e.matchup}</div>
      <div class="event-selection">Open side: <b>${e.selectionAgainst}</b></div>
      <div class="event-card-bottom">
        <div class="event-stake">
          <span class="event-stake-value">${e.stake.toLocaleString()} VC</span>
          <span class="event-stake-label">STAKE</span>
        </div>
        <a href="markets.html" class="btn btn-outline event-accept">Accept Bet</a>
      </div>
    </div>
  `).join("");
}

/* =========================================================
   MOBILE NAV TOGGLE
   ========================================================= */
function initMobileNav() {
  const toggle = document.getElementById("navToggle");
  const nav = document.getElementById("mobileNav");
  if (!toggle || !nav) return;

  toggle.addEventListener("click", () => {
    const isOpen = nav.classList.toggle("is-open");
    toggle.setAttribute("aria-expanded", isOpen ? "true" : "false");
    toggle.setAttribute("aria-label", isOpen ? "Close menu" : "Open menu");
  });
}

/* =========================================================
   INIT
   ========================================================= */
document.addEventListener("DOMContentLoaded", () => {
  buildTicker();
  buildSpotlightSlip();
  buildEventList();
  initMobileNav();
});
