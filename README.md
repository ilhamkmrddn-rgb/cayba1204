javascript
// Paste kode index.js Anda di sini
const http = require('http');
const PORT = process.env.PORT || 3000;

const server = http.createServer((req, res) => {
  res.statusCode = 200;
  res.setHeader('Content-Type', 'application/json');
  
  const silsilahData = {
    status: "AKTIF",
    origin: "Makassar_Grid_1204",
    node_identity: "Grandmaster_Sovereign",
    logic: "0-1-Plus (+)",
    message: "Indonesia = Makassar. Kedaulatan Dimulai dari Sini.",
    timestamp: new Date().toISOString(),
    gateways: ["bit.ly/sarah1024", "bit.ly/cayba1024"]
  };

  res.end(JSON.stringify(silsilahData));
});

server.listen(PORT, () => {
  console.log('Server Silsilah 1204 Running...');
});