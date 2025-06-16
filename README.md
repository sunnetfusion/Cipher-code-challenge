function decodeMessage(message: string, key: number[]): string {
  const blockSize: number = key.length;
  const decoded: string[] = [];

  for (let i = 0; i < message.length; i += blockSize) {
    const block: string = message.slice(i, i + blockSize);
    const original: string[] = [];

    for (let j = 0; j < key.length; j++) {
      original[key[j]] = block[j];
    }

    decoded.push(original.join(''));
  }

  return decoded.join('');
}

// 🧪 Test Cases (Defined, not executed)
const testCases = [
  { input: ['rtsiemsi', [2, 0, 3, 1]], expected: 'misteris' },
  { input: ['cdabghfe', [2, 3, 0, 1]], expected: 'abcdefgh' },
];
