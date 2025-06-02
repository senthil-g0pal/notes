---
type: Data fetching
keywords: react, enquiry, fetch
tags: [react, enquiry, fetch]
---
Uses SWR

Fetcher - Smartfetch - Custom implemenation of fetch api
To prevent race condition and avoid stale response

Create a key and compare it every response, if its same then the response is from current request otherwise ignore.

Attaches CSRF token for every non-get requests

Context API


expose fetcher using ApiContext

fetcher -> ApiContext(create -> provider -> consume using custom hook (useApi))


fetchData -> EnquiryContext (create -> provider -> consume usinh customHook (useEnquuireApi))

Questions?
2 layers of abstraction- why?
fetcher - common fetch code
ENquiry -> uses fetch
