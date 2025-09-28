# Booking API Tests

This repository contains Postman tests for the Restful Booker API, including positive and negative test cases.

## 1. Install dependencies

If you don’t have Newman installed globally:

```bash
npm install -g newman

npx newman run BookingAPI.postman_collection.json -e BookingAPI.postman_environment.json
