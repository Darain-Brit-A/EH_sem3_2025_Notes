# Assignment 12: Serve a Directory using Python

## Aim:
Turn your computer into a simple web server to share files over the internet.

---

## Methodology:

1. **Create a directory** named `webserver` using the `mkdir` command:

    ```bash
    mkdir webserver
    ```

2. **Go into the directory** using the `cd` command:

    ```bash
    cd webserver
    ```

3. **Create an HTML file** named `index.html`. Naming it `index.html` makes the browser open it by default when visiting the root (`/`) path. Otherwise, you'd have to specify the filename in the URL.

    ```bash
    echo '<h1>Local server accessed</h1>' > index.html
    ```

4. **Start the server** using:

    ```bash
    python3 -m http.server 8080
    ```

   <img width="600" height="320" alt="image" src="https://github.com/user-attachments/assets/3d264f8f-f809-4390-ab83-3a5780a9396c" />


5. **Open the browser** and enter:

    ```
    http://localhost:8080
    ```

    This will automatically load and display `index.html`.

   <img width="602" height="319" alt="image" src="https://github.com/user-attachments/assets/4da3e01b-72e8-438e-bdc0-dd5b46954ecd" />


7. **View the terminal logs** to see the web server's activity, which shows requests like GET and their response codes.

    <img width="586" height="357" alt="image" src="https://github.com/user-attachments/assets/c44fe380-ed06-4781-8117-57cb5955867e" />


---

## Findings and Conclusions

- Python’s built-in HTTP server is useful for quickly testing or sharing files locally.  
- The server lacks authentication and encryption, making it unsuitable for public use.  
- Without an `index.html`, a **directory listing** is shown, which can leak file names — a potential **security risk**.  
- Learned how web servers expose files, how clients make HTTP GET requests, and how logs record those interactions.
