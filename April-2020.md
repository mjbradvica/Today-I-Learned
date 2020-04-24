
# 4/5

In CSS, you can hightlight the whole page to see the size and spacing of all elements.

```css
* { background-color: rgba(255,0,0,.2); }
* * { background-color: rgba(0,255,0,.2); }
* * * { background-color: rgba(0,0,255,.2); }
* * * * { background-color: rgba(255,0,255,.2); }
* * * * * { background-color: rgba(0,255,255,.2); }
* * * * * * { background-color: rgba(255,255,0,.2); }
* * * * * * * { background-color: rgba(255,0,0,.2); }
* * * * * * * * { background-color: rgba(0,255,0,.2); }
* * * * * * * * * { background-color: rgba(0,0,255,.2); }
```

#4/24

How to take multiple byte arrays, and return a pdf in C#.

```csharp
public IEnumerable<byte> PdfFilesToZipArchive(IEnumerable<LoanDocument> loanDocuments)
      {
            using (var zipStream = new MemoryStream())
            {
                using (var zipArchive = new ZipArchive(zipStream, ZipArchiveMode.Create, true))
                {
                    foreach (var loanDocument in loanDocuments)
                    {
                        using (var pdfMemoryStream = new MemoryStream(loanDocument.File.ToArray()))
                        {
                            var zipEntry = zipArchive.CreateEntry(loanDocument.FileName);
                            using (var writer = new StreamWriter(zipEntry.Open()))
                            {
                                pdfMemoryStream.WriteTo(writer.BaseStream);
                            }
                        }
                    }
                }

                return zipStream.ToArray();
            }
        }       
```
