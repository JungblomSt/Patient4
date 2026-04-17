# Kodkliniken - Stina Thun

## Patient jag ansvarade för
- Patient 4

## Symptom
- Räknaren nollställdes oväntat och label-ändringar försvann
- Exempel: "När jag navigerade tillbaka och vyn ritades om återställdes count till 0."

## Diagnos
- Vyn ägde inte sin CounterViewModel – utan @State skapas en ny instans varje gång SwiftUI ritar om ContentView, vilket raderar all data.

## Behandling
- Lade till @State på viewModel-deklarationen i ContentView

## Verifiering
- Räknaren behåller sitt värde efter omritningar.

## Lärdomar
@State krävs för att Viewn ska äga och bevara instansen mellan omritningar.
- Saknad @State syns inte som ett kompileringsfel, vilket gör buggen svår att upptäcka utan att testa navigering eller omritning aktivt.
