<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css"
        integrity="sha384-Vkoo8x4CGsO3+Hhxv8T/Q5PaXtkKtu6ug5TOeNV6gBiFeWPGFN9MuhOf23Q9Ifjh" crossorigin="anonymous">
    <title>Website Link Shortner || Pappu Kumar</title>
</head>

<body>
    <div class="container">
        <h1>Make Your Website Tiny</h1>
        <h1>And Share if With Any Where</h1>
        <form action="/shortUrls" method="POST" class="my-4 form-inline">
            <label for="fullUrl" class="sr-only">Url</label>
            <input required placeholder="Url" type="url" name="fullUrl" id="fullUrl" class="form-control col mr-2">
            <button class="btn btn-primary" type="submit">Shrink the link</button>
        </form>

        <table class="table table-striped table-responsive">
            <thead>
                <tr>
                    <th>Full URL</th>
                    <th>Short URL</th>
                    <th>Total Clicks</th>
                </tr>
            </thead>
            <tbody>
                <% shortUrls.forEach(shortUrl => { %>
                <tr>
                    <td><a href="<%= shortUrl.full %>"><%= shortUrl.full %></a></td>
                    <td><a href="<%= shortUrl.short %>"><%= shortUrl.short %></a></td>
                    <td><%= shortUrl.clicks %></td>
                </tr>
                <% }) %>
            </tbody>
        </table>
    </div>
    <div class="container my-5">
        <footer>
            <p>Created by: Jatin namdeo</p>
            <p>Contact information: <a href="mailto:jatin.namdeotkg@gmail.com">
                    jatin.namdeotkg@gmail.com</a>.</p>
        </footer>
    </div>
</body>

</html>
