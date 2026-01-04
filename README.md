# How-to-enable-swagger-UI
first step: add package: Swashbuckle.AspNetCore 7.2.0
second step: add the swagger Ui in program.cs file
if (app.Environment.IsDevelopment())
{
  
    app.UseSwagger();
    app.UseSwaggerUI();
}
third step : builder.Services.AddSwaggerGen(options =>
{
    options.SwaggerDoc("v1", new Microsoft.OpenApi.Models.OpenApiInfo
    {
        Title = "Swagger Demo API",
        Version = "v1",
        Description = "This is a demo app using Swagger in .NET 9."
    });
});
add this before ::::: var app = builder.Build();


then in properties=> go to launchsetting.json file and "launchBrowser": true, i hope you check it is true.

now it is ready to run 
it show error but you need to write /swagger after localhost url like this
http://localhost:5047/swagger/index.html
