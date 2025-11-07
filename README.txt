name: Build Asfar Taxi APK

on:
  push:
    branches:
      - main

jobs:
  build:
    name: Build APK
    runs-on: ubuntu-latest

    steps:
      - name: Checkout repository
        uses: actions/checkout@v3

      - name: Set up JDK 17
        uses: actions/setup-java@v3
        with:
          java-version: '17'
          distribution: 'temurin'

      - name: Grant execute permission for gradlew
        run: chmod +x ./gradlew

      - name: Build release APK
        run: ./gradlew assembleRelease

      - name: Upload APK artifact
        uses: actions/upload-artifact@v3
        with:
          name: Asfar_taxi
          path: app/build/outputs/apk/release/app-release.apk
