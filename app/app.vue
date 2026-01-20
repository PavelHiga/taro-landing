<template>
  <main class="min-h-screen bg-background text-foreground">
    <!-- Top bar -->
    <header class="sticky top-0 z-40 border-b bg-background/80 backdrop-blur">
      <div class="mx-auto flex max-w-6xl items-center justify-between px-4 py-3">
        <div class="flex items-center gap-2">
          <div class="flex h-9 w-9 items-center justify-center rounded-lg border bg-muted">
            🔮
          </div>
          <div class="leading-tight">
            <div class="text-sm font-semibold">TaroGPT</div>
            <div class="text-xs text-muted-foreground">AI-таролог в Telegram</div>
          </div>
        </div>

        <nav class="hidden items-center gap-6 text-sm md:flex">
          <a class="text-muted-foreground hover:text-foreground" href="#how">Как работает</a>
          <a class="text-muted-foreground hover:text-foreground" href="#features">Возможности</a>
          <a class="text-muted-foreground hover:text-foreground" href="#faq">FAQ</a>
        </nav>

        <div class="flex items-center gap-2">
          <a
              :href="telegramLink"
              target="_blank"
              rel="noopener"
              class="inline-flex h-9 items-center justify-center rounded-md bg-primary px-4 text-sm font-medium text-primary-foreground shadow hover:opacity-90"
          >
            Перейти в Telegram
          </a>
        </div>
      </div>
    </header>

    <!-- Hero -->
    <section class="mx-auto max-w-6xl px-4 pb-10 pt-12 md:pb-16 md:pt-16">
      <div class="grid gap-8 md:grid-cols-2 md:items-center">
        <div class="space-y-6">
          <div class="inline-flex items-center gap-2 rounded-full border bg-muted px-3 py-1 text-xs text-muted-foreground">
            ⚡ Ответ ≤ 10 секунд · 🔮 Расклад за 1 минуту
          </div>

          <h1 class="text-balance text-4xl font-bold tracking-tight md:text-5xl">
            Таролог онлайн — <span class="text-primary">TaroGPT</span>
          </h1>

          <p class="text-pretty text-base leading-relaxed text-muted-foreground md:text-lg">
            Получите <strong class="text-foreground">гадание на картах Таро онлайн</strong> с помощью искусственного интеллекта.
            Задайте вопрос — и получите персональное толкование в удобном формате <strong class="text-foreground">Telegram-бота</strong>.
          </p>

          <div class="flex flex-col gap-3 sm:flex-row sm:items-center">
            <a
                :href="telegramLink"
                target="_blank"
                rel="noopener"
                class="inline-flex h-11 items-center justify-center rounded-md bg-primary px-6 text-sm font-semibold text-primary-foreground shadow hover:opacity-90"
            >
              Начать в Telegram
            </a>

            <button
                type="button"
                class="inline-flex h-11 items-center justify-center rounded-md border bg-background px-6 text-sm font-semibold hover:bg-muted"
                @click="scrollTo('#how')"
            >
              Как это работает
            </button>
          </div>

          <div class="grid grid-cols-2 gap-3 pt-2 md:grid-cols-3">
            <div class="rounded-lg border bg-card p-3">
              <div class="text-xs text-muted-foreground">Раскладов</div>
              <div class="text-lg font-semibold">10 000+</div>
            </div>
            <div class="rounded-lg border bg-card p-3">
              <div class="text-xs text-muted-foreground">Пользователей</div>
              <div class="text-lg font-semibold">1 000+</div>
            </div>
            <div class="hidden rounded-lg border bg-card p-3 md:block">
              <div class="text-xs text-muted-foreground">Доступность</div>
              <div class="text-lg font-semibold">24/7</div>
            </div>
          </div>

          <div class="text-xs text-muted-foreground">
            Без регистрации · Без банковских карт · Анонимно
          </div>
        </div>

        <!-- Hero Card -->
        <div class="relative">
          <div class="rounded-2xl border bg-card p-6 shadow-sm">
            <div class="flex items-start justify-between gap-4">
              <div>
                <div class="text-sm font-semibold">Пример запроса</div>
                <div class="mt-1 text-sm text-muted-foreground">
                  «Что меня ждёт в ближайший месяц в работе и финансах?»
                </div>
              </div>
              <div class="rounded-lg border bg-muted px-3 py-1 text-xs text-muted-foreground">Демо</div>
            </div>

            <div class="mt-6 grid gap-3">
              <div class="rounded-xl border bg-background p-4">
                <div class="text-xs text-muted-foreground">🃏 Выпавшие карты</div>
                <div class="mt-2 grid grid-cols-3 gap-2 text-center text-xs">
                  <div class="rounded-lg border bg-muted p-2">
                    <div class="text-base">🜁</div>
                    <div class="mt-1 font-medium">Прошлое</div>
                    <div class="text-muted-foreground">Дурак</div>
                  </div>
                  <div class="rounded-lg border bg-muted p-2">
                    <div class="text-base">🜂</div>
                    <div class="mt-1 font-medium">Настоящее</div>
                    <div class="text-muted-foreground">Маг</div>
                  </div>
                  <div class="rounded-lg border bg-muted p-2">
                    <div class="text-base">🜄</div>
                    <div class="mt-1 font-medium">Будущее</div>
                    <div class="text-muted-foreground">Звезда</div>
                  </div>
                </div>
              </div>

              <div class="rounded-xl border bg-background p-4">
                <div class="text-xs text-muted-foreground">📖 Толкование (пример)</div>
                <p class="mt-2 text-sm leading-relaxed text-muted-foreground">
                  Вы на пороге нового этапа: появляется шанс усилить влияние и взять управление в свои руки.
                  В ближайшее время возможна ясная цель и поддержка обстоятельств — важно действовать последовательно.
                </p>
              </div>

              <a
                  :href="telegramLink"
                  target="_blank"
                  rel="noopener"
                  class="inline-flex h-11 items-center justify-center rounded-md bg-primary px-6 text-sm font-semibold text-primary-foreground shadow hover:opacity-90"
              >
                Получить свой расклад
              </a>
            </div>
          </div>

          <!-- subtle glow -->
          <div class="pointer-events-none absolute -inset-6 -z-10 rounded-[32px] bg-primary/10 blur-3xl"></div>
        </div>
      </div>
    </section>

    <!-- How it works -->
    <section id="how" class="border-t bg-muted/30">
      <div class="mx-auto max-w-6xl px-4 py-12 md:py-16">
        <div class="mb-8 space-y-2">
          <h2 class="text-2xl font-bold md:text-3xl">Как это работает — 3 простых шага</h2>
          <p class="text-muted-foreground">
            Быстро, удобно и прямо в Telegram.
          </p>
        </div>

        <div class="grid gap-4 md:grid-cols-3">
          <div class="rounded-2xl border bg-card p-6 shadow-sm">
            <div class="mb-3 inline-flex h-9 w-9 items-center justify-center rounded-lg border bg-muted text-sm">1</div>
            <div class="text-base font-semibold">Перейдите в Telegram-бота</div>
            <p class="mt-2 text-sm text-muted-foreground">
              Откройте бот и нажмите <strong class="text-foreground">Start</strong>.
            </p>
          </div>

          <div class="rounded-2xl border bg-card p-6 shadow-sm">
            <div class="mb-3 inline-flex h-9 w-9 items-center justify-center rounded-lg border bg-muted text-sm">2</div>
            <div class="text-base font-semibold">Задайте вопрос</div>
            <p class="mt-2 text-sm text-muted-foreground">
              Опишите ситуацию своими словами — AI понимает естественный язык.
            </p>
          </div>

          <div class="rounded-2xl border bg-card p-6 shadow-sm">
            <div class="mb-3 inline-flex h-9 w-9 items-center justify-center rounded-lg border bg-muted text-sm">3</div>
            <div class="text-base font-semibold">Получите расклад</div>
            <p class="mt-2 text-sm text-muted-foreground">
              Следуйте подсказкам и получите подробное толкование за минуту.
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- Features -->
    <section id="features" class="mx-auto max-w-6xl px-4 py-12 md:py-16">
      <div class="mb-8 space-y-2">
        <h2 class="text-2xl font-bold md:text-3xl">Онлайн-гадание на Таро с искусственным интеллектом</h2>
        <p class="text-muted-foreground">
          TaroGPT сочетает классические значения карт Таро и возможности AI, чтобы давать понятные ответы на ваши вопросы.
        </p>
      </div>

      <div class="grid gap-4 md:grid-cols-2 lg:grid-cols-3">
        <div class="rounded-2xl border bg-card p-6 shadow-sm">
          <div class="text-sm font-semibold">💫 Фиксированная цена — 25 Stars</div>
          <p class="mt-2 text-sm text-muted-foreground">
            Начните без регистрации и лишних действий — просто задайте вопрос в Telegram.
          </p>
        </div>

        <div class="rounded-2xl border bg-card p-6 shadow-sm">
          <div class="text-sm font-semibold">⚡ Быстро и удобно</div>
          <p class="mt-2 text-sm text-muted-foreground">
            Ответ обычно приходит за несколько секунд. Всё — в одном чате.
          </p>
        </div>

        <div class="rounded-2xl border bg-card p-6 shadow-sm">
          <div class="text-sm font-semibold">🧠 Понимает любые вопросы</div>
          <p class="mt-2 text-sm text-muted-foreground">
            Любовь, работа, деньги, выбор, будущее — формулируйте естественно.
          </p>
        </div>

        <div class="rounded-2xl border bg-card p-6 shadow-sm">
          <div class="text-sm font-semibold">✨Без сложных настроек</div>
          <p class="mt-2 text-sm text-muted-foreground">
            Не нужно выбирать схемы и параметры — просто задайте вопрос, а TaroGPT сделает всё остальное.</p>
        </div>

        <div class="rounded-2xl border bg-card p-6 shadow-sm">
          <div class="text-sm font-semibold">🤍 Без предвзятости</div>
          <p class="mt-2 text-sm text-muted-foreground">
            AI не осуждает и не навязывает — помогает увидеть ситуацию яснее.
          </p>
        </div>

        <div class="rounded-2xl border bg-card p-6 shadow-sm">
          <div class="text-sm font-semibold">🌙 Доступно 24/7</div>
          <p class="mt-2 text-sm text-muted-foreground">
            Ваш личный таролог всегда на связи прямо в Telegram.
          </p>
        </div>
      </div>

      <!-- Topics -->
      <div class="mt-10 rounded-2xl border bg-card p-6 shadow-sm">
        <div class="flex flex-col gap-6 md:flex-row md:items-center md:justify-between">
          <div>
            <div class="text-base font-semibold">Популярные темы для расклада</div>
            <div class="mt-1 text-sm text-muted-foreground">
              Выберите направление — и сформулируйте вопрос конкретно.
            </div>
          </div>
          <a
              :href="telegramLink"
              target="_blank"
              rel="noopener"
              class="inline-flex h-10 items-center justify-center rounded-md bg-primary px-5 text-sm font-semibold text-primary-foreground shadow hover:opacity-90"
          >
            Задать вопрос
          </a>
        </div>

        <div class="mt-5 grid gap-2 sm:grid-cols-2 lg:grid-cols-4">
          <div class="rounded-xl border bg-muted p-3 text-sm">❤️ Любовь и отношения</div>
          <div class="rounded-xl border bg-muted p-3 text-sm">💼 Работа и карьера</div>
          <div class="rounded-xl border bg-muted p-3 text-sm">💰 Деньги и финансы</div>
          <div class="rounded-xl border bg-muted p-3 text-sm">🔮 Ближайшее будущее</div>
          <div class="rounded-xl border bg-muted p-3 text-sm">⚖️ Выбор и решения</div>
          <div class="rounded-xl border bg-muted p-3 text-sm">🧩 Сложная ситуация</div>
          <div class="rounded-xl border bg-muted p-3 text-sm">💑 Чувства партнёра</div>
          <div class="rounded-xl border bg-muted p-3 text-sm">🌌 Личный путь</div>
        </div>
      </div>
    </section>

    <!-- Bonus -->
    <section class="border-t bg-muted/30">
      <div class="mx-auto max-w-6xl px-4 py-12">
        <div class="grid gap-8 md:grid-cols-2 md:items-center">
          <!-- Left text -->
          <div class="space-y-3">
            <h2 class="text-2xl font-bold md:text-3xl">Готовы начать?</h2>
            <p class="text-muted-foreground">
              Задайте вопрос и получите персональный расклад Таро от AI-таролога прямо в Telegram.
            </p>

            <ul class="mt-4 space-y-2 text-sm">
              <li class="flex items-start gap-2">
                <span class="mt-0.5">💫</span>
                <span><strong class="text-foreground">Фиксированная цена:</strong> 25 Telegram-звёзд за расклад</span>
              </li>
              <li class="flex items-start gap-2">
                <span class="mt-0.5">⚡</span>
                <span><strong class="text-foreground">Быстро:</strong> ответ за несколько секунд</span>
              </li>
              <li class="flex items-start gap-2">
                <span class="mt-0.5">🔒</span>
                <span><strong class="text-foreground">Удобно:</strong> оплата через Telegram Stars</span>
              </li>
            </ul>
          </div>

          <!-- Right card -->
          <div class="rounded-2xl border bg-card p-6 shadow-sm">
            <div class="text-sm font-semibold">Начните в Telegram</div>
            <p class="mt-2 text-sm text-muted-foreground">
              Нажмите кнопку — откроется бот. Затем задайте вопрос и подтвердите оплату Stars.
            </p>

            <div class="mt-5 flex flex-col gap-3 sm:flex-row">
              <a
                  :href="telegramLink"
                  target="_blank"
                  rel="noopener"
                  class="inline-flex h-11 flex-1 items-center justify-center rounded-md bg-primary px-6 text-sm font-semibold text-primary-foreground shadow hover:opacity-90"
              >
                Перейти в Telegram
              </a>

              <button
                  type="button"
                  class="inline-flex h-11 flex-1 items-center justify-center rounded-md border bg-background px-6 text-sm font-semibold hover:bg-muted"
                  @click="copyLink"
              >
                {{ copied ? 'Ссылка скопирована' : 'Скопировать ссылку' }}
              </button>
            </div>

            <p class="mt-4 text-xs text-muted-foreground">
              Совет: сформулируйте запрос конкретно (сфера + что хотите узнать) — так ответ будет точнее.
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- FAQ -->
    <section id="faq" class="mx-auto max-w-6xl px-4 py-12 md:py-12">
      <div class="mb-8 space-y-2">
        <h2 class="text-2xl font-bold md:text-3xl">FAQ</h2>
        <p class="text-muted-foreground">
          Частые вопросы про таро онлайн, Taro AI и Telegram-бота.
        </p>
      </div>

      <div class="grid gap-4 md:grid-cols-2">
        <details class="group rounded-2xl border bg-card p-5 shadow-sm">
          <summary class="cursor-pointer list-none text-sm font-semibold">
            Это гадание Таро онлайн бесплатно?
            <span class="float-right text-muted-foreground group-open:rotate-180">⌄</span>
          </summary>
          <p class="mt-3 text-sm text-muted-foreground">
            Нет. Каждый персональный расклад в TaroGPT стоит 25 Telegram-звёзд. Это фиксированная цена за быстрый и подробный AI-анализ вашего вопроса.</p>
        </details>

        <details class="group rounded-2xl border bg-card p-5 shadow-sm">
          <summary class="cursor-pointer list-none text-sm font-semibold">
            Где проходит расклад — на сайте или в Telegram?
            <span class="float-right text-muted-foreground group-open:rotate-180">⌄</span>
          </summary>
          <p class="mt-3 text-sm text-muted-foreground">
            Сайт — это описание и вход. Сам расклад и диалог происходят в Telegram-боте, чтобы было удобно и быстро.
          </p>
        </details>

        <details class="group rounded-2xl border bg-card p-5 shadow-sm">
          <summary class="cursor-pointer list-none text-sm font-semibold">
            Какие вопросы можно задавать AI-тарологу?
            <span class="float-right text-muted-foreground group-open:rotate-180">⌄</span>
          </summary>
          <p class="mt-3 text-sm text-muted-foreground">
            Любые: любовь, отношения, чувства, работа, деньги, выбор, ближайшее будущее. Чем конкретнее вопрос — тем точнее ответ.
          </p>
        </details>

        <details class="group rounded-2xl border bg-card p-5 shadow-sm">
          <summary class="cursor-pointer list-none text-sm font-semibold">
            Чем TaroGPT отличается от обычного таролога?
            <span class="float-right text-muted-foreground group-open:rotate-180">⌄</span>
          </summary>
          <p class="mt-3 text-sm text-muted-foreground">
            Он доступен 24/7, отвечает быстро, не осуждает и помогает взглянуть на ситуацию с разных сторон, используя значения карт и AI-анализ.
          </p>
        </details>
      </div>

      <div class="mt-10 flex justify-center">
        <a
            :href="telegramLink"
            target="_blank"
            rel="noopener"
            class="inline-flex h-11 items-center justify-center rounded-md bg-primary px-8 text-sm font-semibold text-primary-foreground shadow hover:opacity-90"
        >
          Перейти в Telegram и начать
        </a>
      </div>
    </section>

    <!-- Footer -->
    <footer class="border-t">
      <div class="mx-auto flex max-w-6xl flex-col gap-3 px-4 py-8 md:flex-row md:items-center md:justify-between">
        <div class="text-sm text-muted-foreground">
          © {{ new Date().getFullYear() }} TaroGPT · Таролог онлайн (AI)
        </div>
        <div class="flex flex-wrap items-center gap-4 text-sm">
          <a class="text-muted-foreground hover:text-foreground" :href="telegramLink" target="_blank" rel="noopener">
            Telegram
          </a>
          <a class="text-muted-foreground hover:text-foreground" href="#features">Возможности</a>
          <a class="text-muted-foreground hover:text-foreground" href="#faq">FAQ</a>
        </div>
      </div>
    </footer>
  </main>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const telegramLink = 'https://t.me/taro_ai_app_bot'

const copied = ref(false)

function scrollTo(selector: string) {
  const el = document.querySelector(selector)
  el?.scrollIntoView({ behavior: 'smooth', block: 'start' })
}

async function copyLink() {
  try {
    await navigator.clipboard.writeText(telegramLink)
    copied.value = true
    setTimeout(() => (copied.value = false), 1800)
  } catch {
    // fallback
    copied.value = true
    setTimeout(() => (copied.value = false), 1800)
  }
}
</script>

<style>
:root {
  --background: 0 0% 100%;
  --foreground: 222.2 84% 4.9%;
  --card: 0 0% 100%;
  --card-foreground: 222.2 84% 4.9%;
  --muted: 210 40% 96.1%;
  --muted-foreground: 215.4 16.3% 46.9%;
  --border: 214.3 31.8% 91.4%;
  --primary: 262.1 83.3% 57.8%;
  --primary-foreground: 210 40% 98%;
}

.bg-background { background-color: hsl(var(--background)); }
.text-foreground { color: hsl(var(--foreground)); }
.bg-card { background-color: hsl(var(--card)); }
.text-card-foreground { color: hsl(var(--card-foreground)); }
.bg-muted { background-color: hsl(var(--muted)); }
.text-muted-foreground { color: hsl(var(--muted-foreground)); }
.border { border-color: hsl(var(--border)); }
.bg-primary { background-color: hsl(var(--primary)); }
.text-primary-foreground { color: hsl(var(--primary-foreground)); }
.text-primary { color: hsl(var(--primary)); }
</style>
