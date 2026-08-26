# Operations

## Booking platform

Custom-built single-page app at **app.brattlefly.com**, replacing Acuity Scheduling.

- **Stack:** Vercel (hosting) / Node.js serverless / Google Sheets backend / Square (payments) / Resend (email)
- **Repo:** `brattlefly/booking` on GitHub
- **Features:** admin panel, guide calendar availability blocking, events system (registration, capacity enforcement, paid/free paths, confirmation emails), markdown rendering across content areas, hidden internal test session pattern

### Tracking

- GTM container `GTM-WTJJRCWQ` installed on both brattlefly.com and app.brattlefly.com
- Google Ads conversion tag ("GA - Booking Confirmed - Conversion") fires on a `booking_confirmed` dataLayer event from the payment-success path, gated to exclude free bookings
- `booking_page_viewed` event exists for remarketing
- Meta Pixel ID: `959901570006080`
- **Known cleanup item:** legacy Acuity GTM tags are a potential phantom conversion source and should be removed

## POS & payments

- **Square** — retail and field transactions
- ACH preferred for high-ticket guided trip bookings
- **Square processing fees erode the $1.50 license agent commission** — cash and check are preferable for Vermont fishing license transactions specifically
- **Square "Track by Availability"** is the correct inventory setting for license items

## Accounting

- **QuickBooks Online**
- Vermont fishing license fees are recorded as a **liability** (VT License Fees Payable), not income — only the retained agent commission ($1.50/license for most types) is BrattleFly revenue
- Weekly ACH reconciliation cycle with VT DFW

## Inventory

| Line | Notes |
|---|---|
| Diamondback rods/reels | Purchased outright at 55% wholesale discount (not consignment) |
| Orvis | Wholesale dealer minimum: $6,500 (confirmed with rep; previously misquoted as $7,000) |
| Echo / Maxcatch | Entry tier |
| Terminal tackle & flies | Largest budget allocation, highest margin velocity |
| Boots & waders | Excluded from initial inventory plan |
| Fly tying materials program | Scoped as a future initiative — requires separate external funding |

## Retail

Full retail launched **October 1, 2026** at 45 Linden Street. Guided trips, VT fishing license sales, and events (fly tying nights) were live before that date.

Free casting clinics run as awareness/lead-generation and have produced Google reviews. Echo brand combo kits and practice rods serve as the upsell product alongside them.

## Google Workspace

Set up on the brattlefly.com domain. Backend (Google Sheets, Calendar, Apps Script, GCP Service Account) still runs under the original Gmail account — migration is deliberately deferred to off-season as a low-risk cutover, not attempted during peak season.
