# Match packing list PDFs to purchase orders using docling-serve and Ollama

- **Who’s it for**
  Workflow builders who want to automate the matching of packing-list PDFs against purchase order data locally. It's aimed at people comfortable running local services (n8n, Ollama, docling-serve). This template is presented as a proof-of-concept rather than a production-ready product.

- **How it works / What it does**

1. Monitor pending folder.
   1. It periodically checks a SFTP folder for new PDF files.
2.

- **How to set up**
  Requirements

- **Requirements**
  - SFTP server that has 3 folders:
    - pending
    - completed
    - failed
  - [n8n data table](https://docs.n8n.io/build/work-with-data/data-tables) for logging
  - [Ollama](https://ollama.com/) or other AI service
  - [docling-serve ](https://github.com/docling-project/docling-serve/tree/main)
- **How to customize the workflow**

# Files overview

├── README.md
├── template.json
├── scripts/
│ ├── generate_test_pdfs.py # synthesize packing-list PDFs (clean + OCR-error variants)
│ ├── generate_mock_pos.py # generate matching po-00X.json files
│ ├── validate_output.py # check workflow's extracted JSON against expected schema
│ └── requirements.txt
├── test-files/
│ ├── packing-lists/
│ └── purchase-orders/
├── assets/
│ └── workflow-screenshot.png
└── LICENSE
