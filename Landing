import {
    useState,
    useEffect,
    useRef
}

from "react";

const css=` @import url('https://fonts.googleapis.com/css2?family=Cabinet+Grotesk:wght@400;500;700;800;900&family=DM+Sans:ital,wght@0,300;0,400;0,500;1,300&display=swap');

*,
*::before,
*::after {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

html {
    scroll-behavior: smooth;
}

body {
    background: #111110;
    color: #F0EFED;
    font-family: 'DM Sans', sans-serif;
    overflow-x: hidden;
}

:root {
    --bg: #111110;
    --bg2: #161614;
    --card: #1A1A18;
    --border: #222220;
    --border2: #2A2A28;
    --cream: #FAFAF8;
    --cream2: #F2F0ED;
    --line: #EEECEA;
    --white: #F0EFED;
    --gray: #888;
    --muted: #444;
    --green: #10B981;
    --blue: #3B82F6;
    --ink: #111110;
}

::-webkit-scrollbar {
    width: 3px;
}

::-webkit-scrollbar-track {
    background: var(--bg);
}

::-webkit-scrollbar-thumb {
    background: var(--border2);
}

/* ─── NAV ─────────────────────────────────────────────── */
.nav {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 200;
    height: 60px;
    padding: 0 56px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    background: rgba(250, 250, 248, 0.92);
    backdrop-filter: blur(16px);
    border-bottom: 1px solid var(--line);
    transition: background 0.3s;
}

.nav-logo {
    font-family: 'Cabinet Grotesk', sans-serif;
    font-weight: 900;
    font-size: 17px;
    color: var(--ink);
    letter-spacing: -0.5px;
    cursor: pointer;
}

.nav-links {
    display: flex;
    gap: 32px;
}

.nav-links a {
    font-size: 14px;
    color: #888;
    font-weight: 500;
    cursor: pointer;
    text-decoration: none;
    transition: color 0.2s;
    letter-spacing: -0.1px;
}

.nav-links a:hover {
    color: var(--ink);
}

.nav-right {
    display: flex;
    align-items: center;
    gap: 12px;
}

.nav-ghost {
    padding: 8px 18px;
    background: transparent;
    border: 1px solid #DDDBD8;
    border-radius: 7px;
    font-size: 13px;
    font-weight: 700;
    color: var(--ink);
    cursor: pointer;
    transition: all 0.2s;
    font-family: 'Cabinet Grotesk', sans-serif;
}

.nav-ghost:hover {
    border-color: #999;
}

.nav-cta {
    padding: 8px 18px;
    background: var(--ink);
    color: var(--cream);
    border: none;
    border-radius: 7px;
    font-size: 13px;
    font-weight: 700;
    cursor: pointer;
    transition: opacity 0.2s;
    font-family: 'Cabinet Grotesk', sans-serif;
}

.nav-cta:hover {
    opacity: 0.78;
}

/* ─── HERO ────────────────────────────────────────────── */
.hero {
    background: var(--cream);
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 120px 56px 80px;
    position: relative;
    overflow: hidden;
    border-bottom: 1px solid var(--line);
}

.hero-ring {
    position: absolute;
    border-radius: 50%;
    border: 1px solid var(--line);
    pointer-events: none;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
}

.hero-pill {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 5px 14px 5px 6px;
    border-radius: 100px;
    border: 1px solid var(--line);
    background: #fff;
    font-size: 12px;
    color: #666;
    font-weight: 500;
    margin-bottom: 36px;
    width: fit-content;
}

.hero-pill-icon {
    width: 22px;
    height: 22px;
    border-radius: 50%;
    background: var(--ink);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 11px;
}

.hero-top {
    display: grid;
    grid-template-columns: 1fr 400px;
    gap: 80px;
    align-items: end;
}

.hero h1 {
    font-family: 'Cabinet Grotesk', sans-serif;
    font-size: clamp(52px, 7vw, 84px);
    font-weight: 900;
    line-height: 1.01;
    letter-spacing: -3.5px;
    color: var(--ink);
}

.hero h1 .fade {
    color: #BBBAB8;
}

.hero-right {
    padding-bottom: 6px;
}

.hero-sub {
    font-size: 16px;
    color: #666;
    line-height: 1.8;
    margin-bottom: 32px;
    font-weight: 300;
    max-width: 360px;
}

.hero-btns {
    display: flex;
    gap: 10px;
    flex-wrap: wrap;
    margin-bottom: 0;
}

.btn-dark {
    padding: 13px 26px;
    background: var(--ink);
    color: var(--cream);
    border: none;
    border-radius: 8px;
    font-size: 14px;
    font-weight: 700;
    cursor: pointer;
    transition: opacity 0.2s;
    font-family: 'Cabinet Grotesk', sans-serif;
    display: inline-flex;
    align-items: center;
    gap: 6px;
    letter-spacing: -0.2px;
}

.btn-dark:hover {
    opacity: 0.78;
}

.btn-outline {
    padding: 13px 26px;
    background: transparent;
    color: var(--ink);
    border: 1px solid #DDDBD8;
    border-radius: 8px;
    font-size: 14px;
    font-weight: 700;
    cursor: pointer;
    transition: all 0.2s;
    font-family: 'Cabinet Grotesk', sans-serif;
    letter-spacing: -0.2px;
}

.btn-outline:hover {
    border-color: #999;
}

.hero-numbers {
    display: flex;
    margin-top: 72px;
    border-top: 1px solid var(--line);
    padding-top: 32px;
}

.hero-num {
    flex: 1;
    padding-right: 40px;
    border-right: 1px solid var(--line);
    margin-right: 40px;
}

.hero-num:last-child {
    border-right: none;
    margin-right: 0;
}

.hero-num-v {
    font-family: 'Cabinet Grotesk', sans-serif;
    font-size: 32px;
    font-weight: 900;
    color: var(--ink);
    letter-spacing: -1.5px;
    line-height: 1;
}

.hero-num-l {
    font-size: 12px;
    color: #AAA;
    margin-top: 6px;
    font-weight: 500;
}

/* ─── SHARED SECTION ──────────────────────────────────── */
.section {
    padding: 96px 56px;
    border-bottom: 1px solid var(--border);
}

.section-light {
    background: var(--cream2);
    border-bottom: 1px solid var(--line);
}

.section-eye {
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--muted);
    margin-bottom: 40px;
    font-family: 'Cabinet Grotesk', sans-serif;
}

.section-eye-light {
    color: #AAA;
}

.section-h {
    font-family: 'Cabinet Grotesk', sans-serif;
    font-size: clamp(32px, 4vw, 52px);
    font-weight: 900;
    letter-spacing: -2px;
    line-height: 1.06;
    margin-bottom: 14px;
}

.section-h-dark {
    color: var(--white);
}

.section-h-light {
    color: var(--ink);
}

.section-sub {
    font-size: 16px;
    line-height: 1.75;
    max-width: 440px;
    margin-bottom: 56px;
    font-weight: 300;
}

.section-sub-dark {
    color: #555;
}

.section-sub-light {
    color: #777;
}

/* ─── PAIN ────────────────────────────────────────────── */
.pain-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1px;
    background: var(--border);
}

.pain-card {
    background: var(--bg);
    padding: 40px 32px;
    transition: background 0.2s;
}

.pain-card:hover {
    background: var(--bg2);
}

.pain-n {
    font-family: 'Cabinet Grotesk', sans-serif;
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 2px;
    color: var(--muted);
    text-transform: uppercase;
    margin-bottom: 28px;
}

.pain-card h3 {
    font-family: 'Cabinet Grotesk', sans-serif;
    font-size: 19px;
    font-weight: 800;
    color: var(--white);
    margin-bottom: 12px;
    letter-spacing: -0.5px;
}

.pain-card p {
    font-size: 14px;
    color: #555;
    line-height: 1.8;
    font-weight: 300;
}

.pain-tag {
    margin-top: 24px;
    display: inline-flex;
    align-items: center;
    gap: 6px;
    padding: 5px 12px;
    border-radius: 5px;
    background: rgba(220, 38, 38, 0.06);
    border: 1px solid rgba(220, 38, 38, 0.12);
    font-size: 12px;
    color: #F87171;
    font-weight: 600;
    font-family: 'Cabinet Grotesk', sans-serif;
}

/* ─── STEPS ───────────────────────────────────────────── */
.steps-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 48px;
}

.step-num-box {
    width: 44px;
    height: 44px;
    border-radius: 11px;
    background: var(--border);
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'Cabinet Grotesk', sans-serif;
    font-size: 16px;
    font-weight: 900;
    color: var(--white);
    margin-bottom: 24px;
}

.step h3 {
    font-family: 'Cabinet Grotesk', sans-serif;
    font-size: 19px;
    font-weight: 800;
    color: var(--white);
    margin-bottom: 10px;
    letter-spacing: -0.4px;
}

.step p {
    font-size: 14px;
    color: #555;
    line-height: 1.8;
    font-weight: 300;
}

.step-badge {
    margin-top: 18px;
    display: inline-block;
    padding: 4px 10px;
    border-radius: 5px;
    background: rgba(16, 185, 129, 0.07);
    border: 1px solid rgba(16, 185, 129, 0.14);
    font-size: 11px;
    color: #10B981;
    font-weight: 700;
    letter-spacing: 0.3px;
    font-family: 'Cabinet Grotesk', sans-serif;
}

/* ─── CALCULATOR ──────────────────────────────────────── */
.calc-wrap {
    max-width: 860px;
    margin: 0 auto;
    background: var(--bg2);
    border-radius: 20px;
    border: 1px solid var(--border2);
    padding: 56px;
    position: relative;
    overflow: hidden;
}

.calc-glow {
    position: absolute;
    top: -80px;
    right: -80px;
    width: 300px;
    height: 300px;
    background: radial-gradient(ellipse, rgba(59, 130, 246, 0.06) 0%, transparent 65%);
    pointer-events: none;
}

.calc-head {
    margin-bottom: 48px;
}

.calc-head h3 {
    font-family: 'Cabinet Grotesk', sans-serif;
    font-size: 28px;
    font-weight: 900;
    letter-spacing: -1px;
    color: var(--white);
    margin-bottom: 8px;
}

.calc-head p {
    font-size: 15px;
    color: #555;
    font-weight: 300;
}

.calc-inputs {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
    margin-bottom: 32px;
}

.calc-field label {
    display: block;
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--muted);
    margin-bottom: 10px;
    font-family: 'Cabinet Grotesk', sans-serif;
}

.calc-input {
    width: 100%;
    padding: 13px 16px;
    background: var(--bg);
    border: 1px solid var(--border2);
    border-radius: 8px;
    color: var(--white);
    font-size: 16px;
    font-weight: 500;
    outline: none;
    transition: border-color 0.2s;
    font-family: 'Cabinet Grotesk', sans-serif;
}

.calc-input:focus {
    border-color: #3B82F6;
}

.calc-result {
    padding: 28px 32px;
    border-radius: 12px;
    background: linear-gradient(135deg, rgba(59, 130, 246, 0.07), rgba(16, 185, 129, 0.04));
    border: 1px solid rgba(59, 130, 246, 0.14);
}

.result-row {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 0;
}

.result-item {
    text-align: center;
    padding: 0 24px;
    border-right: 1px solid var(--border2);
}

.result-item:first-child {
    padding-left: 0;
}

.result-item:last-child {
    border-right: none;
    padding-right: 0;
}

.result-v {
    font-family: 'Cabinet Grotesk', sans-serif;
    font-size: 36px;
    font-weight: 900;
    letter-spacing: -1.5px;
    line-height: 1;
    margin-bottom: 8px;
}

.result-v.red {
    color: #F87171;
}

.result-v.green {
    color: #10B981;
}

.result-v.blue {
    color: #60A5FA;
}

.result-l {
    font-size: 12px;
    color: #555;
    font-weight: 500;
    line-height: 1.5;
}

/* ─── PLANS ───────────────────────────────────────────── */
.plans-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
}

.plan-card {
    padding: 36px 32px;
    border-radius: 16px;
    border: 1px solid var(--border);
    background: var(--bg2);
    transition: border-color 0.3s, transform 0.2s;
    position: relative;
    overflow: hidden;
}

.plan-card:hover:not(.plan-feat) {
    border-color: var(--border2);
    transform: translateY(-3px);
}

.plan-feat {
    border-color: var(--white);
    background: var(--white);
}

.plan-tag {
    font-size: 10px;
    font-weight: 700;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--muted);
    margin-bottom: 16px;
    font-family: 'Cabinet Grotesk', sans-serif;
}

.plan-feat .plan-tag {
    color: #AAA;
}

.plan-name {
    font-family: 'Cabinet Grotesk', sans-serif;
    font-size: 22px;
    font-weight: 900;
    color: var(--white);
    letter-spacing: -0.5px;
    margin-bottom: 6px;
}

.plan-feat .plan-name {
    color: var(--ink);
}

.plan-desc {
    font-size: 13px;
    color: #555;
    line-height: 1.6;
    margin-bottom: 24px;
    font-weight: 400;
}

.plan-feat .plan-desc {
    color: #888;
}

.plan-price {
    font-family: 'Cabinet Grotesk', sans-serif;
    font-size: 48px;
    font-weight: 900;
    letter-spacing: -2px;
    line-height: 1;
    color: var(--white);
    margin-bottom: 4px;
}

.plan-feat .plan-price {
    color: var(--ink);
}

.plan-period {
    font-size: 12px;
    color: var(--muted);
    font-weight: 600;
    margin-bottom: 28px;
    font-family: 'Cabinet Grotesk', sans-serif;
}

.plan-feat .plan-period {
    color: #AAA;
}

.plan-line {
    height: 1px;
    background: var(--border);
    margin-bottom: 24px;
}

.plan-feat .plan-line {
    background: #E8E6E3;
}

.plan-feats {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 11px;
    margin-bottom: 32px;
}

.plan-feats li {
    display: flex;
    align-items: flex-start;
    gap: 10px;
    font-size: 13px;
    color: #555;
    line-height: 1.5;
    font-weight: 400;
}

.plan-feat .plan-feats li {
    color: #777;
}

.plan-feats li .chk {
    color: #10B981;
    font-size: 12px;
    font-weight: 900;
    flex-shrink: 0;
    margin-top: 1px;
}

.plan-feat .plan-feats li .chk {
    color: #059669;
}

.plan-btn-outline {
    width: 100%;
    padding: 13px;
    background: transparent;
    border: 1px solid var(--border2);
    border-radius: 9px;
    color: var(--white);
    font-size: 13px;
    font-weight: 700;
    cursor: pointer;
    transition: all 0.2s;
    font-family: 'Cabinet Grotesk', sans-serif;
    letter-spacing: -0.2px;
}

.plan-btn-outline:hover {
    background: var(--border);
}

.plan-btn-dark {
    width: 100%;
    padding: 13px;
    background: var(--ink);
    border: none;
    border-radius: 9px;
    color: var(--cream);
    font-size: 13px;
    font-weight: 700;
    cursor: pointer;
    transition: opacity 0.2s;
    font-family: 'Cabinet Grotesk', sans-serif;
    letter-spacing: -0.2px;
}

.plan-btn-dark:hover {
    opacity: 0.78;
}

.plan-popular {
    position: absolute;
    top: 20px;
    right: 20px;
    padding: 4px 10px;
    border-radius: 100px;
    background: var(--ink);
    font-size: 10px;
    font-weight: 700;
    letter-spacing: 1.5px;
    text-transform: uppercase;
    color: var(--cream);
    font-family: 'Cabinet Grotesk', sans-serif;
}

/* ─── ADDONS ──────────────────────────────────────────── */
.addons-table {
    width: 100%;
    border-collapse: collapse;
}

.addons-table th {
    text-align: left;
    padding: 12px 20px;
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--muted);
    border-bottom: 1px solid var(--border);
    font-family: 'Cabinet Grotesk', sans-serif;
}

.addons-table th:not(:first-child) {
    text-align: center;
}

.addons-table td {
    padding: 16px 20px;
    border-bottom: 1px solid var(--border);
    font-size: 14px;
    color: #666;
    transition: background 0.15s;
}

.addons-table tr:hover td {
    background: var(--bg2);
}

.addons-table tr:last-child td {
    border-bottom: none;
}

.addon-name {
    font-weight: 600;
    color: var(--white);
    font-family: 'Cabinet Grotesk', sans-serif;
    font-size: 14px;
    letter-spacing: -0.2px;
}

.addon-price {
    text-align: center;
    font-family: 'Cabinet Grotesk', sans-serif;
    font-weight: 700;
    font-size: 14px;
    color: var(--white);
}

.addon-monthly {
    text-align: center;
    font-size: 13px;
    color: #555;
}

/* ─── SCORE ───────────────────────────────────────────── */
.score-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 16px;
}

.score-card {
    padding: 28px 24px;
    border-radius: 14px;
    border: 1px solid var(--border);
    background: var(--bg2);
    text-align: center;
    transition: all 0.2s;
}

.score-card:hover {
    border-color: var(--border2);
    transform: translateY(-2px);
}

.score-icon {
    font-size: 22px;
    margin-bottom: 16px;
}

.score-val {
    font-family: 'Cabinet Grotesk', sans-serif;
    font-size: 40px;
    font-weight: 900;
    letter-spacing: -2px;
    line-height: 1;
    margin-bottom: 10px;
}

.score-val.c1 {
    color: #60A5FA;
}

.score-val.c2 {
    color: #10B981;
}

.score-val.c3 {
    color: #F59E0B;
}

.score-val.c4 {
    color: #A78BFA;
}

.score-label {
    font-size: 13px;
    color: #555;
    line-height: 1.5;
    font-weight: 400;
}

/* ─── VERTICALS ───────────────────────────────────────── */
.vert-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1px;
    background: var(--line);
}

.vert-card {
    background: var(--cream2);
    padding: 36px 28px;
    transition: background 0.2s;
    cursor: default;
}

.vert-card:hover {
    background: var(--cream);
}

.vert-icon {
    font-size: 28px;
    margin-bottom: 20px;
}

.vert-card h3 {
    font-family: 'Cabinet Grotesk', sans-serif;
    font-size: 17px;
    font-weight: 800;
    color: var(--ink);
    margin-bottom: 10px;
    letter-spacing: -0.4px;
}

.vert-card p {
    font-size: 13px;
    color: #888;
    line-height: 1.7;
    font-weight: 400;
}

.vert-price {
    margin-top: 20px;
    font-family: 'Cabinet Grotesk', sans-serif;
    font-size: 18px;
    font-weight: 900;
    color: var(--ink);
    letter-spacing: -0.5px;
}

.vert-monthly {
    font-size: 12px;
    color: #AAA;
    font-weight: 500;
    margin-top: 2px;
}

/* ─── FAQ ─────────────────────────────────────────────── */
.faq-list {
    max-width: 680px;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    gap: 1px;
    background: var(--border);
    border-radius: 12px;
    overflow: hidden;
}

.faq-item {
    background: var(--bg2);
}

.faq-q {
    padding: 20px 24px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    cursor: pointer;
    transition: background 0.15s;
    font-size: 15px;
    font-weight: 500;
    color: var(--white);
    font-family: 'Cabinet Grotesk', sans-serif;
    letter-spacing: -0.2px;
    user-select: none;
}

.faq-q:hover {
    background: var(--card);
}

.faq-q.open {
    color: var(--cream);
}

.faq-arrow {
    color: var(--muted);
    font-size: 16px;
    transition: transform 0.25s;
    flex-shrink: 0;
}

.faq-arrow.open {
    transform: rotate(180deg);
    color: var(--white);
}

.faq-a {
    padding: 0 24px 20px;
    font-size: 14px;
    color: #555;
    line-height: 1.8;
    font-weight: 300;
}

/* ─── CTA FINAL ───────────────────────────────────────── */
.cta {
    padding: 96px 56px;
    background: var(--cream2);
    border-top: 1px solid var(--line);
}

.cta-inner {
    max-width: 580px;
    margin: 0 auto;
    text-align: center;
}

.cta h2 {
    font-family: 'Cabinet Grotesk', sans-serif;
    font-size: clamp(36px, 5vw, 56px);
    font-weight: 900;
    letter-spacing: -2.5px;
    color: var(--ink);
    line-height: 1.04;
    margin-bottom: 14px;
}

.cta h2 span {
    color: #BBBAB8;
}

.cta p {
    font-size: 16px;
    color: #888;
    margin-bottom: 44px;
    font-weight: 300;
    line-height: 1.7;
}

.cta-form {
    display: flex;
    flex-direction: column;
    gap: 10px;
}

.cta-row {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 10px;
}

.cta-input {
    padding: 14px 18px;
    background: #fff;
    border: 1px solid var(--line);
    border-radius: 9px;
    color: var(--ink);
    font-size: 14px;
    font-weight: 500;
    outline: none;
    transition: border-color 0.2s;
    font-family: 'Cabinet Grotesk', sans-serif;
    width: 100%;
}

.cta-input:focus {
    border-color: #999;
}

.cta-input::placeholder {
    color: #CCC;
    font-weight: 400;
}

.cta-submit {
    padding: 15px;
    background: var(--ink);
    color: var(--cream);
    border: none;
    border-radius: 9px;
    font-size: 14px;
    font-weight: 700;
    cursor: pointer;
    transition: opacity 0.2s;
    font-family: 'Cabinet Grotesk', sans-serif;
    letter-spacing: -0.2px;
    width: 100%;
}

.cta-submit:hover {
    opacity: 0.78;
}

.cta-note {
    font-size: 12px;
    color: #CCC;
    margin-top: 12px;
}

/* ─── FOOTER ──────────────────────────────────────────── */
.footer {
    padding: 28px 56px;
    background: var(--bg);
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-top: 1px solid var(--border);
}

.footer-logo {
    font-family: 'Cabinet Grotesk', sans-serif;
    font-size: 14px;
    font-weight: 900;
    color: var(--white);
    letter-spacing: -0.4px;
}

.footer-links {
    display: flex;
    gap: 24px;
}

.footer-links a {
    font-size: 12px;
    color: var(--muted);
    cursor: pointer;
    text-decoration: none;
    transition: color 0.2s;
}

.footer-links a:hover {
    color: #666;
}

.footer-copy {
    font-size: 12px;
    color: var(--muted);
}

/* ─── WA BUTTON ───────────────────────────────────────── */
.wa-btn {
    position: fixed;
    bottom: 28px;
    right: 28px;
    z-index: 500;
    width: 54px;
    height: 54px;
    border-radius: 50%;
    background: #25D366;
    border: none;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 24px;
    box-shadow: 0 4px 20px rgba(37, 211, 102, 0.3);
    transition: transform 0.2s, box-shadow 0.2s;
}

.wa-btn:hover {
    transform: scale(1.08);
    box-shadow: 0 6px 28px rgba(37, 211, 102, 0.45);
}

/* ─── ANIMATIONS ──────────────────────────────────────── */
@keyframes fadeUp {
    from {
        opacity: 0;
        transform: translateY(20px);
    }

    to {
        opacity: 1;
        transform: translateY(0);
    }
}

.fu {
    animation: fadeUp 0.55s ease both;
}

.d1 {
    animation-delay: 0.05s;
}

.d2 {
    animation-delay: 0.15s;
}

.d3 {
    animation-delay: 0.28s;
}

.d4 {
    animation-delay: 0.42s;
}

.d5 {
    animation-delay: 0.56s;
}

/* ─── RESPONSIVE ──────────────────────────────────────── */
@media (max-width: 960px) {
    .nav {
        padding: 0 24px;
    }

    .nav-links {
        display: none;
    }

    .hero {
        padding: 100px 24px 64px;
    }

    .hero-top {
        grid-template-columns: 1fr;
        gap: 40px;
    }

    .hero-sub {
        max-width: 100%;
    }

    .hero-numbers {
        flex-wrap: wrap;
        gap: 24px;
    }

    .hero-num {
        border-right: none;
        padding-right: 0;
        margin-right: 0;
        border-bottom: 1px solid var(--line);
        padding-bottom: 24px;
    }

    .section {
        padding: 64px 24px;
    }

    .pain-grid,
    .steps-grid,
    .plans-grid,
    .score-grid,
    .vert-grid {
        grid-template-columns: 1fr;
    }

    .calc-wrap {
        padding: 32px 24px;
    }

    .calc-inputs {
        grid-template-columns: 1fr;
    }

    .result-row {
        grid-template-columns: 1fr;
        gap: 16px;
    }

    .result-item {
        border-right: none;
        padding: 0;
        border-bottom: 1px solid var(--border2);
        padding-bottom: 16px;
    }

    .result-item:last-child {
        border-bottom: none;
        padding-bottom: 0;
    }

    .cta {
        padding: 64px 24px;
    }

    .cta-row {
        grid-template-columns: 1fr;
    }

    .footer {
        padding: 24px;
        flex-direction: column;
        gap: 16px;
        text-align: center;
    }

    .footer-links {
        flex-wrap: wrap;
        justify-content: center;
    }
}

`;

function useCountUp(target, duration=1800) {
    const [val,
    setVal]=useState(0);
    const ref=useRef(null);
    const started=useRef(false);

    useEffect(()=> {
            const el=ref.current;
            if ( !el) return;
            let t;

            const obs=new IntersectionObserver(([e])=> {
                    if (e.isIntersecting && !started.current) {
                        started.current=true;
                        const steps=duration / 16;
                        const inc=target / steps;
                        let cur=0;

                        t=setInterval(()=> {
                                cur +=inc;

                                if (cur >=target) {
                                    setVal(target); clearInterval(t);
                                }

                                else setVal(Math.floor(cur));
                            }

                            , 16);
                    }
                }

                , {
                threshold: 0.3
            });
        obs.observe(el);

        return ()=> {
            obs.disconnect();
            if (t) clearInterval(t);
        }

        ;
    }

    , [target, duration]);
return [val,
ref];
}

const faqs=[ {
    q: "¿Cuánto tiempo tarda la implementación?", a: "Pack Start: 5-7 días hábiles. Pack Pro: 10-12 días. Enterprise:
 según el alcance acordado. Tu operación sigue igual durante todo el proceso." },
 {
        q: "¿Tengo que instalar algo en mis computadoras?", a: "No. Todo corre en nuestros servidores. Tu equipo accede al
 panel desde cualquier navegador, en cualquier dispositivo, sin instalar nada." },
 {
            q: "¿Qué pasa si hay un corte de luz o internet en mi empresa?", a: "Nada. Operamos en infraestructura en la nube
 distribuida geográficamente, independiente de la electricidad o internet local. Tus automatizaciones corren igual." },
 {
                q: "¿Mis datos son seguros? ¿A quién pertenecen?", a: "Tus datos son exclusivamente tuyos. Los almacenamos en
 servidores dedicados a tu empresa, nunca los compartimos y puedes exportarlos completos en cualquier momento." },
 {
                    q: "¿Puedo pagar en bolívares?", a: "Sí. Aceptamos USD, EUR y bolívares digitales. Para pagos en Bs. aplicamos la tasa
 BCV oficial del día con ventana de pago de 24 horas." },
 {
                        q: "¿El mantenimiento mensual es obligatorio?", a: "No. El pago de implementación es único. El mantenimiento es
 completamente opcional y puedes cancelarlo cuando quieras sin penalizaciones." },
];

                        const addons=[ {
                            name: "Zyncro Bot con IA", desc: "Asistente entrenado con tu negocio, activo 24/7", impl: "$400", mo: "$120/mes"
                        }

                        ,
                        {
                        name: "Monitor de Competencia", desc: "Reporte semanal de precios y movimientos del sector", impl: "$200", mo: "$80/mes"
                    }

                    ,
                    {
                    name: "Automatización de Reclutamiento", desc: "Clasifica CVs, agenda entrevistas automáticamente", impl: "$280", mo: "$90/mes"
                }

                ,
                {
                name: "Portal para clientes finales", desc: "Cada cliente tuyo ve su estado en tiempo real", impl: "$500", mo: "$150/mes"
            }

            ,
            {
            name: "Alertas de Tipo de Cambio", desc: "Notificación instantánea al cruzar tus umbrales BCV", impl: "$150", mo: "$40/mes"
        }

        ,
        {
        name: "Módulo SENIAT / Fiscal", desc: "Recordatorios, IVA automático y reportes para el contador", impl: "$400", mo: "$100/mes"
    }

    ,
    {
    name: "Integración Punto de Venta", desc: "POS físico conectado al ecosistema Zyncro", impl: "$400", mo: "$100/mes"
}

,
{
name: "Cobranza Inteligente", desc: "Recordatorios en escalada para facturas vencidas", impl: "$250", mo: "$70/mes"
}

,
];

const verticals=[ {
    icon: "🏥", title: "Clínicas y consultorios", desc: "Citas, lista de espera, historial y cobros en dólares
 automatizados.", price: "$650", mo: "$175/mes" },
 {
        icon: "🏗️", title: "Inmobiliarias", desc: "Seguimiento de leads, cuotas en construcción y documentos de cierre.",
            price: "$750", mo: "$150/mes"
    }

    ,
    {
    icon: "🏫", title: "Colegios privados", desc: "Mensualidades, comunicados masivos y reportes de asistencia.", price: "$650", mo: "$140/mes"
}

,
{
icon: "🔧", title: "Talleres mecánicos", desc: "Estado del vehículo en tiempo real y recordatorios de mantenimiento.",
    price: "$550", mo: "$120/mes"
}

,
{
icon: "✈️", title: "Agencias de viaje", desc: "Confirmaciones, itinerarios automáticos y alertas de vuelo.", price: "$600", mo: "$120/mes"
}

,
{
icon: "🤝", title: "Iglesias y ONGs", desc: "Comunicación masiva, eventos y gestión de contribuciones.", price: "$320", mo: "$80/mes"
}

,
];

export default function ZyncroLanding() {
    const [emp,
    setEmp]=useState(5);
    const [hrs,
    setHrs]=useState(12);
    const [sal,
    setSal]=useState(400);
    const [openFaq,
    setOpenFaq]=useState(null);

    // Estado para el formulario CTA
    const [formData,
    setFormData]=useState({
        nombre: '', empresa: '', whatsapp: '', dolor: ''
    });
const [formStatus,
setFormStatus]=useState('idle'); // idle, loading, success, error

const handleFormSubmit=async (e)=> {
    e.preventDefault();
    setFormStatus('loading');

    try {
        // URL de pruebas de tu Webhook de n8n
        const webhookUrl='https://zyncro.app.n8n.cloud/webhook-test/lead';

        const response=await fetch(webhookUrl, {

            method: 'POST',
            headers: {
                'Content-Type': 'application/json'
            }

            ,
            body: JSON.stringify(formData)
        });

    if (response.ok) {
        setFormStatus('success');

        setFormData({
            nombre: '', empresa: '', whatsapp: '', dolor: ''
        });
}

else {
    throw new Error('Network response was not ok');
}
}

catch (error) {
    console.error("Error enviando datos:", error);
    setFormStatus('error');
}
}

;

const handleFormChange=(e)=> {
    setFormData({
        ...formData, [e.target.name]: e.target.value
    });
}

;

const costo=Math.round(emp * hrs * 4 * (sal / 160));
const ahorro=Math.round(costo * 0.72);
const roi=costo>0 ? Math.round((ahorro / 350) * 100) : 0;

const [v1,
r1]=useCountUp(1240);
const [v2,
r2]=useCountUp(847);
const [v3,
r3]=useCountUp(93);
const [v4,
r4]=useCountUp(28);

return (<> <style> {
        css
    }

    </style> {
        /* NAV */
    }

    <nav className="nav" > <div className="nav-logo" >Zyncro</div> <div className="nav-links" > <a href="#servicios" >Servicios</a> <a href="#precios" >Precios</a> <a href="#verticales" >Sectores</a> <a href="#faq" >FAQ</a> </div> <div className="nav-right" > <button className="nav-ghost" >Ver demo</button> <button className="nav-cta" >Hablar con nosotros →</button> </div> </nav> {
        /* HERO */
    }

    <section className="hero" id="inicio" > {
        [800, 1200, 1600].map(s=> (<div key= {
                    s
                }

                className="hero-ring" style= {
                        {
                        width: s, height: s
                    }
                }

                />))
    }

    <div className="hero-pill fu d1" > <div className="hero-pill-icon" ><span>⚡</span></div> Automatización inteligente para Venezuela </div> <div className="hero-top" > <div> <h1 className="fu d2" > Deja de pagar<br /> <span className="fade" >con tiempo</span><br /> lo que es gratis. </h1> <div className="hero-numbers fu d5" > {
        [["1,240+", "horas ahorradas al mes"], ["$0", "suscripciones obligatorias"], ["5–7", "días promedio de
 entrega"]].map(([v,l],i)=>(
 <div className="hero-num" key= {
            i
        }

        > <div className="hero-num-v" > {
            v
        }

        </div> <div className="hero-num-l" > {
            l
        }

        </div> </div>))
}

</div></div><div className="hero-right fu d3"><p className="hero-sub">Tu equipo pierde horas en tareas que pueden hacerse solas. Nosotros las eliminamos. Sin software complicado,
sin suscripciones obligatorias.</p><div className="hero-btns"><button className="btn-dark">Ver cómo funciona →</button><button className="btn-outline">Hablar con nosotros</button></div></div></div></section> {
    /* PAIN */
}

<section className="section" id="servicios"><div className="section-eye">El problema</div><h2 className="section-h section-h-dark">Cada tarea manual<br />tiene un precio oculto.</h2><p className="section-sub section-sub-dark">Y casi nadie lo calcula hasta que lo ve en números reales.</p><div className="pain-grid"> {
    [ {
        n: "01", title:"Pedidos manuales", desc:"Alguien copia cada pedido de WhatsApp a Excel. Un error y un
 cliente perdido. Horas de trabajo que desaparecen.", cost:" ~$300 USD/mes perdidos" },
 {
            n: "02", title:"Reportes del viernes", desc:"El gerente espera el informe que alguien prepara 3 horas
 antes. Sin datos en tiempo real para decidir.", cost:" ~$400 USD/mes perdidos" },
 {
                n: "03", title:"Cobranza olvidada", desc:"Facturas vencidas sin recordatorio. Clientes que no pagan porque
 nadie les avisó. Flujo de caja impredecible.", cost:" ~$500 USD/mes perdidos" },
].map((c, i)=>(<div className="pain-card" key= {
                            i
                        }

                        > <div className="pain-n" > {
                            c.n
                        }

                        </div> <h3> {
                            c.title
                        }

                        </h3> <p> {
                            c.desc
                        }

                        </p> <div className="pain-tag" >⚠ {
                            c.cost
                        }

                        </div> </div>))
            }

            </div></section> {
                /* STEPS */
            }

            <section className="section" style= {
                    {
                    background: "var(--bg2)"
                }
            }

            ><div className="section-eye">El proceso</div><h2 className="section-h section-h-dark">Tres pasos.<br />Sin fricción.</h2><p className="section-sub section-sub-dark">De la primera llamada al sistema funcionando en menos de dos semanas.</p><div className="steps-grid"> {
                [ {
                    n: "1", title:"Discovery", desc:"30 minutos. Mapeamos tu operación e identificamos exactamente qué
 automatizaríamos y cuánto te ahorraría.", badge:" 1-2 días" },
 {
                        n: "2", title:"Construcción", desc:"Construimos en nuestros servidores. Tú no instalas nada. Probamos con
 datos reales antes de activar.", badge:" 5-12 días hábiles" },
 {
                            n: "3", title:"Entrega", desc:"Panel web activo, video de formación grabado y documentación completa. El
 sistema trabaja mientras duermes.", badge:" Día 1 en producción" },
].map((s, i)=>(<div className="step" key= {
                                        i
                                    }

                                    > <div className="step-num-box" > {
                                        s.n
                                    }

                                    </div> <h3> {
                                        s.title
                                    }

                                    </h3> <p> {
                                        s.desc
                                    }

                                    </p> <div className="step-badge" >⏱ {
                                        s.badge
                                    }

                                    </div> </div>))
                        }

                        </div></section> {
                            /* CALCULATOR */
                        }

                        <section className="section"><div className="section-eye">Calculadora</div><h2 className="section-h section-h-dark">¿Cuánto te está costando<br />no automatizar?</h2><p className="section-sub section-sub-dark">Ajusta los valores y ve el impacto en tiempo real.</p><div className="calc-wrap"><div className="calc-glow" /><div className="calc-head"><h3>Calcula tu ahorro mensual</h3><p>Estimación basada en el costo real de horas de trabajo manual</p></div><div className="calc-inputs"><div className="calc-field"><label>Empleados en tareas manuales</label><input className="calc-input" type="number" value= {
                            emp
                        }

                        min= {
                            1
                        }

                        max= {
                            100
                        }

                        onChange= {
                            e=>setEmp(Math.max(1, +e.target.value))
                        }

                        /></div><div className="calc-field"><label>Horas manuales por semana</label><input className="calc-input" type="number" value= {
                            hrs
                        }

                        min= {
                            1
                        }

                        max= {
                            80
                        }

                        onChange= {
                            e=>setHrs(Math.max(1, +e.target.value))
                        }

                        /></div><div className="calc-field"><label>Salario mensual promedio (USD)</label><input className="calc-input" type="number" value= {
                            sal
                        }

                        min= {
                            50
                        }

                        step= {
                            50
                        }

                        onChange= {
                            e=>setSal(Math.max(50, +e.target.value))
                        }

                        /></div></div><div className="calc-result"><div className="result-row"><div className="result-item"><div className="result-v red">$ {
                            costo.toLocaleString()
                        }

                        </div><div className="result-l">Costo mensual actual<br />en procesos manuales</div></div><div className="result-item"><div className="result-v green">$ {
                            ahorro.toLocaleString()
                        }

                        </div><div className="result-l">Ahorro estimado<br />con Zyncro / mes</div></div><div className="result-item"><div className="result-v blue"> {
                            roi
                        }

                        %</div><div className="result-l">ROI en el primer mes<br />sobre la implementación</div></div></div></div></div></section> {
                            /* PLANS */
                        }

                        <section className="section" id="precios" style= {
                                {
                                background: "var(--bg2)"
                            }
                        }

                        ><div className="section-eye">Planes</div><h2 className="section-h section-h-dark">Un precio justo.<br />Sin sorpresas.</h2><p className="section-sub section-sub-dark">Pago único de implementación. Mantenimiento completamente opcional. </p><div className="plans-grid"> {
                            [ {
                                tag: "START", name:"Pack Start", desc:"PYMES, tiendas y comercio electrónico que reciben pedidos por redes
 sociales.", price:" 350", feats:[" Captura pedidos WhatsApp e Instagram"," Confirmación automática al cliente"," Bot de preguntas frecuentes 24/7"," Recuperación de carritos abandonados"," Catálogo automático por WhatsApp"," Reseñas post-compra automatizadas"," Panel web personalizado"," 30 días soporte incluidos"],
 featured:false
                            }

                            ,
                            {
                            tag: "PRO", name:"Pack Pro", desc:"Empresas de servicios con operaciones multimoneda e inventario activo.",
                                price:"750", feats:["Todo el Pack Start incluido", "Conciliación BCV automática diaria", "Inventario
 sincronizado en tiempo real"," Cobranza inteligente en escalada"," Reportes ejecutivos cada lunes"," Generación automática de propuestas PDF"," Reporte de rentabilidad por cliente"," SLA respuesta en 4 horas hábiles"],
 featured:true
                        }

                        ,
                        {
                        tag: "ENTERPRISE", name:"Enterprise", desc:"Fábricas, grupos industriales y empresas con procesos
 complejos.", price:" 1, 500+", feats:[" Todo el Pack Pro incluido"," Cadena de mando digital"," Módulo SENIAT / fiscal completo"," BI básico con proyecciones"," Módulo de auditoría y trazabilidad"," Dashboard con tu identidad visual"," Formación en vivo con tu equipo"," Monitoreo 24/7 con alertas preventivas"],
 featured:false
                    }

                    ,
                    ].map((pl, i)=>(<div className= {
                                `plan-card $ {
                                    pl.featured?"plan-feat":""
                                }

                                `
                            }

                            key= {
                                i
                            }

                            > {
                                pl.featured && <div className="plan-popular" >Más popular</div>
                            }

                            <div className="plan-tag" > {
                                pl.tag
                            }

                            </div> <div className="plan-name" > {
                                pl.name
                            }

                            </div> <div className="plan-desc" > {
                                pl.desc
                            }

                            </div> <div className="plan-price" >$ {
                                pl.price
                            }

                            </div> <div className="plan-period" >USD · pago único</div> <div className="plan-line" /> <ul className="plan-feats" > {
                                pl.feats.map((f, j)=><li key= {
                                        j
                                    }

                                    ><span className="chk" >✓</span> {
                                        f
                                    }

                                    </li>)
                            }

                            </ul> {
                                pl.featured ? <button className="plan-btn-dark" >Empezar ahora →</button> : <button className="plan-btn-outline" >Ver detalles →</button>
                            }

                            </div>))
                }

                </div></section> {
                    /* ADD-ONS */
                }

                <section className="section"><div className="section-eye">Servicios adicionales</div><h2 className="section-h section-h-dark">Amplía tu sistema<br />cuando quieras.</h2><p className="section-sub section-sub-dark">Disponibles para cualquier plan. Se contratan por separado.</p><table className="addons-table"><thead><tr><th>Servicio</th><th>Implementación</th><th>Mantenimiento mensual</th></tr></thead><tbody> {
                    addons.map((a, i)=>(<tr key= {
                                i
                            }

                            > <td> <div className="addon-name" > {
                                a.name
                            }

                            </div> <div style= {
                                    {
                                    fontSize:12, color:"#444", marginTop:3
                                }
                            }

                            > {
                                a.desc
                            }

                            </div> </td> <td className="addon-price" > {
                                a.impl
                            }

                            </td> <td className="addon-monthly" > {
                                a.mo
                            }

                            </td> </tr>))
                }

                </tbody></table></section> {
                    /* VERTICALS */
                }

                <section className="section section-light" id="verticales"><div className="section-eye section-eye-light">Sectores especializados</div><h2 className="section-h section-h-light">Construido para<br />tu industria.</h2><p className="section-sub section-sub-light">Packs diseñados específicamente para cada sector. Más rápido,
                más preciso.</p><div className="vert-grid"> {
                    verticals.map((v, i)=>(<div className="vert-card" key= {
                                i
                            }

                            > <div className="vert-icon" > {
                                v.icon
                            }

                            </div> <h3> {
                                v.title
                            }

                            </h3> <p> {
                                v.desc
                            }

                            </p> <div className="vert-price" > {
                                v.price
                            }

                            USD</div> <div className="vert-monthly" > {
                                v.mo
                            }

                            mantenimiento opcional</div> </div>))
                }

                </div></section> {
                    /* ZYNCRO SCORE */
                }

                <section className="section" style= {
                        {
                        background: "var(--bg2)"
                    }
                }

                ><div className="section-eye">Zyncro Score</div><h2 className="section-h section-h-dark">Ves el valor en tiempo real.<br />No en promesas.</h2><p className="section-sub section-sub-dark">Tu panel muestra en números exactos cuánto genera Zyncro para tu empresa cada mes.</p><div className="score-grid"> {
                    [ {
                        icon: "⏱", val:v1, ref:r1, cls:"c1", label:"Horas recuperadas\neste mes"
                    }

                    ,
                    {
                    icon: "🛡", val:v2, ref:r2, cls:"c2", label:"Errores evitados\nesta semana"
                }

                ,
                {
                icon: "💵", val:v3, ref:r3, cls:"c3", label:"Miles USD ahorrados\neste trimestre"
            }

            ,
            {
            icon: "⚡", val:v4, ref:r4, cls:"c4", label:"Sistemas activos\nahora mismo"
        }

        ,
        ].map((m, i)=>(<div className="score-card" key= {
                    i
                }

                ref= {
                    m.ref
                }

                > <div className="score-icon" > {
                    m.icon
                }

                </div> <div className= {
                    `score-val $ {
                        m.cls
                    }

                    `
                }

                > {
                    m.val.toLocaleString()
                }

                </div> <div className="score-label" style= {
                        {
                        whiteSpace:"pre-line"
                    }
                }

                > {
                    m.label
                }

                </div> </div>))
    }

    </div></section> {
        /* FAQ */
    }

    <section className="section" id="faq"><div style= {
            {
            textAlign: "center"
        }
    }

    ><div className="section-eye" style= {
            {
            justifyContent: "center", display:"flex"
        }
    }

    >FAQ</div><h2 className="section-h section-h-dark" style= {
            {
            textAlign: "center", marginBottom:14
        }
    }

    >Preguntas frecuentes </h2><p className="section-sub section-sub-dark" style= {
            {
            margin: "0 auto 56px", textAlign:"center"
        }
    }

    >Lo que más nos preguntan antes de arrancar. </p></div><div className="faq-list"> {
        faqs.map((f, i)=>(<div className="faq-item" key= {
                    i
                }

                > <div className= {
                    `faq-q $ {
                        openFaq===i?"open":""
                    }

                    `
                }

                onClick= {
                    ()=>setOpenFaq(openFaq===i?null:i)
                }

                > {
                    f.q
                }

                <span className= {
                    `faq-arrow $ {
                        openFaq===i?"open":""
                    }

                    `
                }

                >▾</span> </div> {
                    openFaq===i && <div className="faq-a" > {
                        f.a
                    }

                    </div>
                }

                </div>))
    }

    </div></section> {
        /* CTA FINAL */
    }

    <section className="cta"><div className="cta-inner"><div className="section-eye section-eye-light" style= {
            {
            textAlign: "center", display:"block", marginBottom:24
        }
    }

    >¿Listo para empezar? </div><h2>Diagnóstico gratis.<br /><span>En 24 horas.</span></h2><p>Cuéntanos tu operación. Sin compromiso. Te decimos exactamente qué automatizaríamos y cuánto ahorrarías. </p><form className="cta-form" onSubmit= {
        handleFormSubmit
    }

    ><div className="cta-row"><input className="cta-input" name="nombre" value= {
        formData.nombre
    }

    onChange= {
        handleFormChange
    }

    placeholder="Tu nombre" required /><input className="cta-input" name="empresa" value= {
        formData.empresa
    }

    onChange= {
        handleFormChange
    }

    placeholder="Empresa" required /></div><input className="cta-input" name="whatsapp" value= {
        formData.whatsapp
    }

    onChange= {
        handleFormChange
    }

    placeholder="WhatsApp" required /><input className="cta-input" name="dolor" value= {
        formData.dolor
    }

    onChange= {
        handleFormChange
    }

    placeholder="¿Cuál es tu mayor dolor operativo ahora mismo?" required /> {
        formStatus==='success' ? (<div style= {
                    {
                    padding: '15px', background: 'rgba(16,185,129,0.1)', color: '#10B981', borderRadius: '9px', fontWeight: 'bold'
                }
            }

            > ¡Solicitud enviada con éxito ! Te contactaremos pronto. </div>) : formStatus==='error' ? (<div style= {
                    {
                    padding: '15px', background: 'rgba(239,68,68,0.1)', color: '#EF4444', borderRadius: '9px', fontWeight: 'bold'
                }
            }

            > Hubo un error al enviar. Por favor intenta de nuevo. </div>) : (<button type="submit" className="cta-submit" disabled= {
                formStatus==='loading'
            }

            style= {
                    {
                    opacity: formStatus==='loading' ? 0.7 : 1
                }
            }

            > {
                formStatus==='loading' ? 'Enviando...' : 'Quiero mi diagnóstico gratis →'
            }

            </button>)
    }

    </form><p className="cta-note">Sin spam. Sin ventas agresivas. Solo claridad.</p></div></section> {
        /* FOOTER */
    }

    <footer className="footer"><div className="footer-logo">Zyncro</div><div className="footer-links"><a>hola@zyncro.app</a><a>@zyncro_app</a><a>Privacidad</a><a>Términos</a></div><div className="footer-copy">© 2025 Zyncro. Todos los derechos reservados.</div></footer> {
        /* WA BUTTON */
    }

    <button className="wa-btn" title="WhatsApp">💬</button></>);
}
