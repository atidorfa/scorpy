<svelte:head>
    <meta charset="utf-8" />
    <script src="https://unpkg.com/pdf-lib"></script>
</svelte:head>


<script>
    createPdf();
    async function createPdf() {
      const pdfDoc = await PDFLib.PDFDocument.create();
      const page = pdfDoc.addPage([350, 400]);
      page.moveTo(110, 200);
      page.drawText('Hello World!');
      const pdfDataUri = await pdfDoc.saveAsBase64({ dataUri: true });
      document.getElementById('pdf').src = pdfDataUri;
    }
  </script>
<div>
    <iframe id="pdf" title="asprin" style="width: 100%; height: 100%;"></iframe>    
</div>

<style>
    div{
         height: 900px;
         width: 100%;
    }

    iframe {
        width: 60%;
        height: 100%;
    }
</style>