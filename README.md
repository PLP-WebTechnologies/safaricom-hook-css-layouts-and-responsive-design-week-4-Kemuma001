# Assignment: Responsive Web Design

Create a responsive webpage using modern CSS techniques, specifically Flexbox, Grid, and Media Queries. The goal is to ensure the webpage adapts gracefully to various screen sizes.

           ## Assignment Tasks

           ### Designing a Responsive Layout
              a. Create a webpage with the following sections:

              Header (including a logo and navigation links).
              Main content area (with two columns: one for text content and the other for an image).
              Footer (with links to social media and a copyright notice).
              b. Use Flexbox to style the navigation menu in the header.
              c. Use CSS Grid to structure the main content area.


                             <!DOCTYPE html>
                                <html lang="en">
                                  <head>
                                          <meta charset="UTF-8">
                                         <meta name="viewport" content="width=device-width, initial-scale=1.0">
                                         <title>Responsive Layout</title>
                                         <link rel="stylesheet" href="styles.css">
                                                    </head>
                                                           <body>
                                                                    <header>
                                                                        <div class="logo">Logo</div>
                                                                             <nav>
                                                                            <ul>
                                                                             <li><a href="#home">Home</a></li>
                                                                             <li><a href="#about">About</a></li>
                                                                             <li><a href="#services">Services</a></li>
                                                                             <li><a href="#contact">Contact</a></li>
                                                                          </ul>
                                                                           </nav>
                                                              </header>
                                                           <main>
                                                        <section class="content">
                                                            <article>
                                                             <h1>Main Content</h1>
                                                                 <p>This is the main text content area.</p>
                                                              </article>
                                                                    <aside>
                                                                      <img src="image.jpg" alt="Sample Image">
                                                                            </aside>
                                                                         </section>
                                                                         </main>
                                                                   <footer>
                                                                         <p>&copy; 2025 Your Website. All rights reserved.</p>
                                                                         <div class="social-media">
                                                                            <a href="#facebook">Facebook</a>
                                                                            <a href="#twitter">Twitter</a>
                                                                            <a href="#instagram">Instagram</a>
                                                                           </div>
                                                                               </footer>
                                                                                    </body>
                                                                                     </html>





                                  * {
                                      margin: 0;
                                     padding: 0;
                                    box-sizing: border-box;
                                      }

                                 body {
                                    font-family: Arial, sans-serif;
                                    line-height: 1.6;
                                           }

                               header {
                                     display: flex;
                                     justify-content: space-between;
                                     align-items: center;
                                    padding: 1rem;
                                    background-color: #333;
                                    color: white;
                                     }

                              header .logo {
                                   font-size: 1.5rem;
                                          }
                              header nav ul {
                                    display: flex;
                                    list-style: none;
                                         }

                              header nav ul li {
                                     margin-left: 1rem;
                                             }

                          header nav ul li a {
                                    color: white;
                                    text-decoration: none;
                                                }

                              main {
                                    padding: 2rem;
                                          }                    

                          main .content {
                                     display: grid;
                                    grid-template-columns: 2fr 1fr;
                                    gap: 1rem;
                                       }

                         footer {
                                    display: flex;
                                    justify-content: space-between;
                                    align-items: center;
                                    padding: 1rem;
                                    background-color: #333;
                                    color: white;
                                           }

                       footer .social-media a {
                                     color: white;
                                     margin-right: 1rem;
                                     text-decoration: none;
                                                }



### Creating Media Queries for Responsiveness
a. Implement media queries to ensure the webpage looks good on the following screen sizes:

Small screens (up to 600px): Stack all sections vertically.
Medium screens (601px to 1024px): Keep the header and footer horizontal, but stack the main content columns.
Large screens (above 1024px): Display the layout as designed with Flexbox and Grid.



                       /* Base Styles */

                              * {
                                   margin: 0;
                                   padding: 0;
                                   box-sizing: border-box;
                                        }

                             body {
                                    font-family: Arial, sans-serif;
                                    line-height: 1.6;
                                            }

                              header {
                                      display: flex;
                                      justify-content: space-between;
                                       align-items: center;
                                       padding: 1rem;
                                       background-color: #333;
                                       color: white;
                                        }

                            header .logo {
                                        font-size: 1.5rem;
                                          }

                            header nav ul {
                                           display: flex;
                                           list-style: none;
                                                 }

                            header nav ul li {
                                             margin-left: 1rem;
                                                    }

                             header nav ul li a {
                                           color: white;
                                           text-decoration: none;
                                                   }

                                 main {
                                               padding: 2rem;
                                                      }

                            main .content {
                                              display: grid;
                                              grid-template-columns: 2fr 1fr;
                                              gap: 1rem;
                                                 }

                              footer {
                                                  display: flex;
                                                  justify-content: space-between;
                                                  align-items: center;
                                                  padding: 1rem;
                                                  background-color: #333;
                                                  color: white;
                                                      }

                             footer .social-media a {
                                                   color: white;
                                                   margin-right: 1rem;
                                                   text-decoration: none;
                                                             }

                           /* Small screens (up to 600px) */
                             @media (max-width: 600px) {
                           header {
                                 flex-direction: column;
                                  align-items: flex-start;
                                      }

                            header nav ul {
                                 flex-direction: column;
                                  align-items: flex-start;
                                      }

                            main .content {
                                      grid-template-columns: 1fr;
                                             }

                            footer {
                                         flex-direction: column;
                                         align-items: flex-start;
                                             }
                                     }

                              /* Medium screens (601px to 1024px) */
                                 @media (min-width: 601px) and (max-width: 1024px) {
                                            main .content {
                                                       grid-template-columns: 1fr;
                                                          }
                                            }

                                             /* Large screens (above 1024px) */
                                                      @media (min-width: 1025px) {
                                                            }


### Bonus

Add animations or transitions when resizing the screen.
/* Base Styles */

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    transition: all 0.3s ease-in-out; /* Add transition to all elements */
}

body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
}

header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem;
    background-color: #333;
    color: white;
    transition: all 0.3s ease-in-out; /* Add transition */
}

header .logo {
    font-size: 1.5rem;
}

header nav ul {
    display: flex;
    list-style: none;
    transition: all 0.3s ease-in-out; /* Add transition */
}

header nav ul li {
    margin-left: 1rem;
}

header nav ul li a {
    color: white;
    text-decoration: none;
}

main {
    padding: 2rem;
    transition: all 0.3s ease-in-out; /* Add transition */
}

main .content {
    display: grid;
    grid-template-columns: 2fr 1fr;
    gap: 1rem;
    transition: all 0.3s ease-in-out; /* Add transition */
}

footer {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem;
    background-color: #333;
    color: white;
    transition: all 0.3s ease-in-out; /* Add transition */
}

footer .social-media a {
    color: white;
    margin-right: 1rem;
    text-decoration: none;
}

/* Small screens (up to 600px) */
@media (max-width: 600px) {
    header {
        flex-direction: column;
        align-items: flex-start;
    }

    header nav ul {
        flex-direction: column;
        align-items: flex-start;
    }

    main .content {
        grid-template-columns: 1fr;
    }

    footer {
        flex-direction: column;
        align-items: flex-start;
    }
}

/* Medium screens (601px to 1024px) */
@media (min-width: 601px) and (max-width: 1024px) {
    main .content {
        grid-template-columns: 1fr;
    }
}

/* Large screens (above 1024px) */
@media (min-width: 1025px) {
    /* No changes needed, the base styles will apply */
}

