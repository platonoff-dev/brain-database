#Web #ClientServer #Security
Cross-site request forgery

Cross-site request forgery, also known as one-click attack or session riding. Abbreviated as *CSRF* .

Is a type of exploit of a website where unauthorized commands are submitted from a user that the web application trusts. CSRF exploits the trust that a site has in a user browser. 

#### Example:####
User got masked link (image, form)


Prevention:

- Synchronize token pattern: [[CSRF Token]]
- Cookie to header token. 
- Double Submit Cookie
- SameSite Cookie attribute
- Client-side safeguards