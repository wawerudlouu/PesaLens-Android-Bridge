# PesaLens Android Bridge

Native Android companion for the PesaLens Personal M-Pesa Finance Dashboard.

## Flow

M-Pesa SMS → PesaLens Bridge → PesaLens API → Dashboard

## Pairing

1. Open the PesaLens web dashboard.
2. Use **Connect Android** and generate the pairing code.
3. Install/run this Android app.
4. Enter the PesaLens URL and pairing code.
5. Grant **Receive SMS** permission.
6. Keep the companion installed. Incoming M-Pesa SMS messages are parsed locally and only structured transaction data is sent to PesaLens.

## Security

- Android token is stored using AndroidX encrypted shared preferences.
- Raw SMS text is not uploaded.
- M-Pesa PINs and OTPs are not requested or transmitted.
- Server-side duplicate protection uses the transaction code.

## Build

Open this folder in Android Studio, let Gradle sync, then use:
Build → Build Bundle(s) / APK(s) → Build APK(s)

Android Studio documents that a debug APK is signed and ready for installation/testing.
