# Airline Logo API – logostream

The **logostream Airline API** provides high-quality logos for over 900+ airlines worldwide. It is specifically designed for travel applications, booking platforms, and Flight Information Display Systems (FIDS).

## 🚀 Features

- **900+ Airlines:** Comprehensive global coverage.
- **Multiple Variants:** Access icons, full wordmarks, or aircraft tail designs.
- **Format Support:** High-quality output including SVG, PNG, JPG, and WebP.
- **Dark Mode Ready:** Includes specific variants for dark backgrounds.
- **Standardized Access:** Simple queries using ICAO codes.

---

## 🔑 Requesting an API Key

A personal API key is required to use the service.
1. Send an email to [sales@logostream.dev](mailto:sales@logostream.dev) or go got https://logostream.dev
2. Include your **intended use case** (e.g., Booking App, FIDS) and the **domain(s)** that will use the API.

---

## 🛠 Usage & Endpoints

**Base URL:** `https://airlines-api.logostream.dev/airlines/`

### Get Logo by ICAO Code
The API currently prioritizes the 3-letter ICAO airline code.

**Endpoint Structure:** `GET /icao/:code?key=YOUR_API_KEY&variant=:variant&radius=:radius`

### Parameters

| Parameter | Type | Description |
| :--- | :--- | :--- |
| `code` | Path | 3-letter ICAO airline code (e.g., `DLH`, `BAW`, `UAE`). |
| `key` | Query | Your personal API key (required). |
| `variant` | Query | Logo style variant (see below). Defaults to `default`. |
| `radius` | Query | Border radius in pixels (e.g., `8`, `16`, or `9999` for circles). |

### Available Variants (`variant`)

* `default`: Square icon (Default).
* `logo`: Full logo including the airline wordmark.
* `tail`: The vertical stabilizer (tail) design of the aircraft.
* `logo-transparent`: Full logo with a transparent background.
* `logo-white`: White version of the logo for dark backgrounds.
* `logo-bg-white`: Logo centered on a white background.
* `icon-transparent`: Icon variant with a transparent background.

---
### cURL Example
To fetch an airline logo via the terminal, use the following command:

bash
curl -X GET "[https://airlines-api.logostream.dev/airlines/icao/AFR?key=YOUR_API_KEY&variant=logo-transparent](https://airlines-api.logostream.dev/airlines/icao/AFR?key=YOUR_API_KEY&variant=logo-transparent)"

## 📝 Examples

### HTML Integration
```html
<img src="[https://airlines-api.logostream.dev/airlines/icao/DLH?key=YOUR_API_KEY&radius=16](https://airlines-api.logostream.dev/airlines/icao/DLH?key=YOUR_API_KEY&radius=16)" alt="Lufthansa" width="64">

<img src="[https://airlines-api.logostream.dev/airlines/icao/BAW?key=YOUR_API_KEY&variant=logo](https://airlines-api.logostream.dev/airlines/icao/BAW?key=YOUR_API_KEY&variant=logo)" alt="British Airways">

<img src="[https://airlines-api.logostream.dev/airlines/icao/UAE?key=YOUR_API_KEY&variant=tail](https://airlines-api.logostream.dev/airlines/icao/UAE?key=YOUR_API_KEY&variant=tail)" alt="Emirates Tail">



