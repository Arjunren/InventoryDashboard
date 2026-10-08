# Inventory Dashboard

## Overview

A responsive inventory-operations dashboard for stock value, low-stock risk, warehouse product search, movement trends, category mix, and simulated stock receiving.

## Features

Asynchronous inventory loading, live summary metrics, CSS/SVG trend visualizations, product search and category/risk filters, stock statuses, reorder context, interactive receiving dialog, responsive tables, and warehouse navigation.

## Technology Stack

React 19, TypeScript 7, Vite 8, Lucide icons, Testing Library, Vitest 5, Nginx, and Docker.

## Requirements / Installation

Install Node.js 24+ and npm 11+, then run `npm install`.

## Environment Variables

`VITE_API_BASE_URL` is documented in `.env.example`. Never place database credentials or private tokens in browser variables.

## Database Setup

This runnable frontend uses `src/services/inventoryApi.ts` as its mock data boundary and requires no database.

## Running the Application

Run `npm run dev`; create production assets with `npm run build`.

## Running Tests

Run `npm run check`. Tests cover data loading, low-stock filtering, and inventory receiving.

## Default Development Accounts

The fictional development persona is Yuki Chen, Inventory Manager. Authentication belongs in the production backend.

## API Endpoints

A production backend should expose authorized summary, product, warehouse, movement, and transactional stock-receipt resources beneath `VITE_API_BASE_URL`.

## Folder Structure

`components` contains inventory table/dialog views, `services` is the API boundary, `types` contains contracts, and `tests` covers user workflows.

## Security Notes

React escapes product data and the demo stores no secrets. Browser totals, role visibility, and stock validation are not security controls: a backend must enforce roles, validate quantities, use atomic inventory transactions, prevent replay/duplicate references, log every adjustment, and return minimum-necessary data.

## Known Limitations

Barcode scanning, supplier purchase orders, serial/lot tracking, multi-currency valuation, offline mode, and real warehouse APIs are outside scope.

## License

MIT
