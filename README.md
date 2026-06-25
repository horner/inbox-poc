
https://docs.google.com/document/d/1YYCBtpLCjBeLjI9ieCUXF5u4azKMC8aan9UAF2nowmU/edit?tab=t.0

# Goal

Replace Document Queue, Fax Queue, File Queue to System Inbox.  The old systems need to be replaced with something that is mobile friendly, less complicated, and flexible to support different workflows.  We should treat all inbox like functions: Scanning, Faxing, Interface documents, Email, Direct Emails, etc. in a consistent and intuitive screen.

## **1.1 Document Paths**

There should be 3 basic paths for incoming documents to come into WebChart:

### **1.1.1 ESIGN**

We know the document chart b/c of an identifier in the document or metadata (mime headers, HL7 PID etc)

* These documents should just be attached to the proper chart and esign requests should be generated based on esign rules (another ticket to simplify this).  
* These documents do not have an system INBOX and are just referenced here for awareness, that not everything goes to a system INBOX.


  ### **1.1.2 PARTITION INBOX**

  These are temporary charts created to hold documents. We don't know the chart b/c the meta data is not there, has not been seen before, or it is unclear as to "which chart" it should map to.


  Examples, include:

* MR numbers in HL7 data that we have not seen  
* Faxes (without metadata)


  ### **1.1.3 CHART INBOX** 

  These are permanent charts used as just a SYSTEM inbox to move documents from the chart to the final destination chart.


  Some Charts may be useful to hold documents where a temporary chart is not practical.  For example, a chart for each fax number could be created to old incoming faxes until the fax is identified for a Patient or Employer Chart.




This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.
