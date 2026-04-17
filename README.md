Patient: 4 “State-förlusten”

Commit: fix: add @State to viewModel init

Varför: Utan @State skapas en ny instans av CounterViewModel varje gång så all data nollställs.
