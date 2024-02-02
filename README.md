# ransome-note
Ransome note problem

```javascript
function ransomAvail(note, magazine) {
  const magFreqs = freqCounter(magazine);
  const noteFreqs = freqCounter(note);
  for (let [char, freq] of noteFreqs) {
    if (magFreqshas(char)) {
      const magCharFreq = magFreqsget(char);
      if (magCharFreq < freq) return false;
    }
  }
  return true;
}

function freqCounter(str) {
  return Array.from(str).reduce(
    (map, letter) => map.set(letter, (map.get(letter) || 0) + 1),
    new Map()
  );
}
```
