# ClerkStore Landing

Landing page for a Telegram-based store that sells access to AI services and subscriptions. The project was prepared as a portfolio case for freelance marketplaces: a compact commercial page with product cards, clear calls to action, FAQ, lightweight animations, and Docker deployment.

## Stack

- Astro 5
- Tailwind CSS
- Vanilla JavaScript for UI interactions
- Docker + nginx for production build

## Features

- Responsive landing page for desktop and mobile
- Sticky navigation with mobile menu
- Product catalog with prices and Telegram purchase flow
- Modal window for checkout redirect
- FAQ section
- Scroll reveal animations
- Card hover glow and tilt interaction
- Optimized static build served by nginx
- Example reverse proxy configuration for VPS deployment

## Project Structure

```text
.
|-- deploy/
|   |-- docker-compose.example.yml
|   `-- nginx.example.conf
|-- public/
|   |-- favicon.svg
|   `-- logo.png
|-- src/
|   |-- pages/index.astro
|   `-- styles/global.css
|-- Dockerfile
|-- nginx.conf
|-- astro.config.mjs
|-- tailwind.config.mjs
`-- package.json
```

## Local Development

```bash
npm install
npm run dev
```

The dev server starts at:

```text
http://localhost:4321
```

## Production Build

```bash
npm run build
npm run preview
```

## Docker

Build and run the static site:

```bash
docker build -t clerkstore-landing .
docker run --rm -p 8080:80 clerkstore-landing
```

Open:

```text
http://localhost:8080
```

## VPS Deployment Example

The `deploy/` folder contains an example Docker Compose setup with an nginx reverse proxy:

```bash
docker compose -f deploy/docker-compose.example.yml up -d --build
```

Before production use, replace `example.com` in `deploy/nginx.example.conf` with your domain and add HTTPS through Cloudflare, Caddy, Traefik, or certbot.

## Portfolio Notes

This project demonstrates a complete landing page workflow:

- visual layout and responsive frontend
- Telegram-first conversion path
- static site generation
- Docker packaging
- VPS/nginx deployment pattern

It is a good fit for Kwork services such as landing page development, Telegram bot storefront pages, small business websites, and simple VPS deployment.

## Описание на русском

ClerkStore Landing - это аккуратный коммерческий лендинг для Telegram-магазина с продажей доступа к AI-сервисам и подпискам. Проект сделан как портфолио-кейс для фриланс-площадок: есть карточки товаров, понятные CTA-кнопки, блок FAQ, анимации появления, модальное окно оформления и пример Docker/nginx-деплоя.

Что внутри:

- адаптивная вёрстка под desktop и mobile
- каталог товаров с ценами и переходом в Telegram-бота
- модальное окно для оформления заказа
- блок FAQ
- анимации при скролле и hover-эффекты на карточках
- статическая сборка через Astro
- пример production-деплоя через Docker и nginx

Этот репозиторий удобно показывать заказчикам на Kwork как пример лендинга под ключ, страницы для Telegram-магазина, коммерческого сайта малого бизнеса или простого VPS-проекта.
