# Timeline - Vertical Resume/Profile Builder

A drop-in pastebin-style timeline editor with dual-sided vertical layout, PGP end-to-end encryption, and PDF export to A4 format.

## Features

- **Dual-sided Timeline**: Professional qualifications (left) + Personal qualifications (right)
- **Vertical Layout**: Multiple configurable horizontal sections
- **PGP E2E Security**: Sign & encryption keys stored separately
- **PDF Export**: A4-formatted vertical timeline with DOM CSS2 PHP library
- **No-JS Support**: Plain PHP JSON fallback rendering
- **TOTP**: Two-factor authentication on save
- **Turnstile**: CAPTCHA integration
- **PSR Router**: Directory-based routing via `/l/<username>`
- **Editor Access**: Edit via published link with signature verification
- **Vanilla Frontend**: ES 1.5 compatible XHR, CSS2 styling

## Stack

- **Backend**: PHP 8.5, MySQL/SQLite with Phinx migrations
- **Frontend**: Vanilla JavaScript (ES 1.5), CSS2
- **Auth**: OpenPGP PHP (vanilla library, no bindings)
- **PDF**: DOM CSS2 PHP library
- **OTP**: TOTP implementation

## Access Points

- `/l/<username>` - View timeline
- `/edit/<username>` - Editor & publisher
- `/publish` - Publish timeline (POST)
- `/edit/delete/<username>` - Delete timeline
- No-JS fallback available

## Installation

1. Create `.env` from `.env.example`
2. Install dependencies: `composer install`
3. Configure database in `.env`
4. Run migrations: `vendor/bin/phinx migrate`
5. Start server: `php -S localhost:8000 -t public`

## Documentation

See `/docs` for configuration, API endpoints, and styling guide.
