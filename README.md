# 100 prisoners

A TypeScript simulation of the 100 prisoners problem.

Each prisoner has a number. The numbers are shuffled into boxes, and every prisoner may open up to half of the boxes looking for their own number. The group is freed only if all of them find it. If everyone opens boxes at random, the group almost never wins.

The script uses the loop-following strategy. A prisoner opens the box that matches their own number, then opens the box whose number was inside the previous one, and keeps following that chain. In theory this wins about 31% of the time. The script plays many rounds and prints how many the group won.

## Running

```bash
npx tsx prison.ts [prisoners] [replays]
```

Both arguments are optional and default to 100 prisoners and 1000 replays. A run with `npx tsx prison.ts 100 2000` won 653 of 2000 rounds (32.65%).
