const utilities = [
    { address: "123 Main St", utility: "Idaho Falls Power" },
    { address: "456 Oak Ave", utility: "Rocky Mountain Power" }
];

document.getElementById('lookupBtn').addEventListener('click', () => {
    const input = document.getElementById('addressInput').value.trim().toLowerCase();
    const match = utilities.find(u => u.address.toLowerCase() === input);
    
    document.getElementById('result').innerText = 
        match ? `Utility: ${match.utility}` : "No matching utility found";
});
