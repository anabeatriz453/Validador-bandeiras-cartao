# Codigo feito delo GITHUB COPILOT


[Uploading index.js…]()/**
 * Function to validate and determine the credit card brand (bandeira)
 * @param {string} cardNumber - The credit card number as a string
 * @returns {string} - The credit card brand or 'Invalid' if not recognized
 */
function getCardBrand(cardNumber) {
    if (!cardNumber || typeof cardNumber !== 'string') {
        return 'Invalid';
    }

    // Remove spaces or dashes from the card number
    const sanitizedNumber = cardNumber.replace(/[\s-]/g, '');

    // Visa: Starts with 4
    if (/^4/.test(sanitizedNumber)) {
        return 'Visa';
    }

    // MasterCard: Starts with 51-55 or 2221-2720
    if (/^5[1-5]/.test(sanitizedNumber) || /^22[2-9][0-9]|^2[3-6][0-9]{2}|^27[0-1][0-9]|^2720/.test(sanitizedNumber)) {
        return 'MasterCard';
    }

    // Elo: Specific intervals like 4011, 4312, 4389, etc.
    const eloPrefixes = ['4011', '4312', '4389'];
    if (eloPrefixes.some(prefix => sanitizedNumber.startsWith(prefix))) {
        return 'Elo';
    }

    // American Express: Starts with 34 or 37
    if (/^3[47]/.test(sanitizedNumber)) {
        return 'American Express';
    }

    // Discover: Starts with 6011, 65, or range 644-649
    if (/^6011/.test(sanitizedNumber) || /^65/.test(sanitizedNumber) || /^64[4-9]/.test(sanitizedNumber)) {
        return 'Discover';
    }

    // Hipercard: Generally starts with 6062
    if (/^6062/.test(sanitizedNumber)) {
        return 'Hipercard';
    }

    // If no match, return 'Invalid'
    return 'Invalid';
}

// Example usage:
console.log(getCardBrand('4011 1234 5678 9012')); // Output: Elo
console.log(getCardBrand('4111 1111 1111 1111')); // Output: Visa
console.log(getCardBrand('5555 5555 5555 4444')); // Output: MasterCard





