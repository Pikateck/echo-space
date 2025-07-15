# 🔥 Razorpay Payment Testing Guide

## 📋 Test Card Details

### ✅ **Successful Payment Cards**

**Primary Test Card (Visa):**

- **Card Number**: `4111 1111 1111 1111`
- **Expiry Date**: `12/25` (any future date)
- **CVV**: `123` (any 3-digit number)
- **Cardholder Name**: `Test User` (any name)

**Alternative Success Cards:**

- **Mastercard**: `5555 5555 5555 4444`
- **American Express**: `3782 8224 6310 005`
- **Visa Debit**: `4000 0560 0000 0004`

### ❌ **Failed Payment Card (for testing failures)**

- **Card Number**: `4000 0000 0000 0002`
- **Expiry**: Any future date
- **CVV**: Any 3-digit number

## 🚀 Testing Flow

### Step 1: Navigate to Payment

1. Go to hotel details page
2. Click "View Deals" or use "Bargain" feature
3. Click "Proceed to Booking"
4. Fill in guest details
5. Reach payment step

### Step 2: Test Payment

1. Use any test card above
2. Click "Complete Payment & Booking"
3. Razorpay popup will appear
4. Enter test card details
5. Click "Pay Now"

### Step 3: After Successful Payment

You will be redirected to **Booking Voucher** with:

- ✅ Payment confirmation
- 🆔 Razorpay Payment ID
- 📄 Complete booking details

### Step 4: View Invoice

From the voucher page, click **"View Invoice"** to see:

- 📊 Detailed invoice with payment info
- 💰 Complete price breakdown
- 🧾 Tax and billing details

## 📄 Available Documents After Payment

1. **📋 Booking Voucher** (`/booking-voucher`)

   - Booking confirmation
   - Hotel details
   - Guest information
   - Payment status

2. **🧾 Booking Invoice** (`/booking-invoice`)
   - Formal invoice document
   - Tax breakdown
   - Billing information
   - Payment confirmation

## 🔄 Test Scenarios

### Scenario A: Regular Booking + Online Payment

- Choose regular room price
- Select "Pay Now"
- Complete Razorpay payment
- View voucher & invoice

### Scenario B: Bargained Booking (Mandatory Payment)

- Use bargain feature
- Automatic "Pay Now" (no pay-at-hotel option)
- Complete Razorpay payment
- View voucher & invoice with discount

### Scenario C: Failed Payment

- Use failed payment card: `4000 0000 0000 0002`
- Payment will fail
- Error message displayed
- Can retry with valid card

## 💡 Notes

- All test payments are free
- No real money charged
- Use test mode credentials: `rzp_test_A2z34SBOQPEI`
- Payment IDs will be in format: `pay_xxxxxxxxxxxxx`
