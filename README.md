# EntityFramework - FluentAPI and DataAnnotations

Two CRUD projects that I made as a class project.At first I started learning the fundemental logic of .NET Core and moved onto the first project.I started writing the code by the right EF work flows, first the Console output project which where you can Create a post,Create a comment,Create a user(Menu 8),Edit and Delete.

# DataAnnotations
****.DBContext Class****

The Data-Base Context class is connecting to SQL via the OnConfiguring method which contains a DbContextOptionsBuilder object where I can connect into the Data-Base
 objectName.UseSqlServer("Server=localhost\\SQLEXPRESS;Database=Data-Base;Trusted_Connection=True;MultipleActiveResultSets=True;");
 
![DataAnnotationContext](https://user-images.githubusercontent.com/80118008/129154550-5c5d6482-fd82-46fb-87a9-9a07f58d185c.PNG)

**.The Class's**

The Posts Class is now being writing and I am using here* DataAnnotations method so for example Post_Id will be the PrimaryKey in the Table so I will use [Key] one line above.
After giving each column its type I open up NuGet PMC and add-migration,update-database.

![DataAnnotation](https://user-images.githubusercontent.com/80118008/129145704-fb56d844-1d56-463a-a9d7-128f35469433.PNG)

--------------------------------------------------------------
# FluentAPI
**.Fluent Class's**

After using Data Annotations I created two new class's both with the same columns and values as in Posts and Comments class's only now I remove all [annotations].
Now I can create a new Class called FluentPostConfig which will inherit from IEntityTypeConfiguration interface using .Metadata.Builders
And now I use the Configure method which contains a generic EntityTypeBuilder object and now I can start using the Fluent code,for example like before I want Post_Id to be my PK so I can write now objectName.HasKey(p => p.Post_Id);

![fluentAPI](https://user-images.githubusercontent.com/80118008/129149864-727efbbc-db4d-49f5-8dde-4750aec7f814.PNG)
* the lambada expression will indicate that Post_Id column is the PrimaryKey of the table.

**.DBContext Class**

The Data-Base Context class uses the same DataBase Set properties only now I wont be using the OnConfiguring method I will use the OnModelCreating method which contains a ModelBuilder object which will apply configurations to the Data-Base so in the code I am using the FluentConfig class's that I made before because I want to stay as orginaized as I can.

![fluentAPIContext](https://user-images.githubusercontent.com/80118008/129154580-f79d5831-a01c-4f4b-93d2-e5483fb211b4.PNG)

--------------------------------------------------------------

# Second Project - WinForms CRUD (no delete option yet)

![1](https://user-images.githubusercontent.com/80118008/129153752-3e59b468-a0c9-4ccd-a351-787cfe1e0e66.PNG)
--------------------------------------------------------------
![2](https://user-images.githubusercontent.com/80118008/129148304-f2c17c5e-a789-478b-bbd2-60aca4fba971.PNG)
--------------------------------------------------------------
![3](https://user-images.githubusercontent.com/80118008/129148305-204b519b-6a49-4dff-b220-4fa08cece738.PNG)
--------------------------------------------------------------
![4](https://user-images.githubusercontent.com/80118008/129148306-784d2062-4cef-495d-93de-8891e2933527.PNG)
--------------------------------------------------------------
![5](https://user-images.githubusercontent.com/80118008/129148307-f31ccf3d-7066-46a8-a71f-7fd6b2968b59.png)
--------------------------------------------------------------
![6](https://user-images.githubusercontent.com/80118008/129148308-558c19a7-ef86-44cb-8cf4-2a9bddc7f7ba.png)
--------------------------------------------------------------
![7](https://user-images.githubusercontent.com/80118008/129148309-cb890d0f-0ddc-476f-96d4-77f3b362ce15.png)


# First Project - Console CRUD

![0](https://user-images.githubusercontent.com/80118008/129153047-22fb2746-8314-462c-9b62-074893aa3f3e.PNG)
-----------------------------------------------------------------------------------------
![2](https://user-images.githubusercontent.com/80118008/129153049-e288d559-6d50-4cbc-ba5d-0c0c9137cebb.PNG)
-----------------------------------------------------------------------------------------
![3](https://user-images.githubusercontent.com/80118008/129153051-a4e714df-776d-4092-b603-95d15e7093d2.PNG)
-----------------------------------------------------------------------------------------
![6](https://user-images.githubusercontent.com/80118008/129153052-2b52ffb8-d898-4f72-ac59-358c0e3274d5.PNG)
-----------------------------------------------------------------------------------------
![8](https://user-images.githubusercontent.com/80118008/129153055-11791e8d-e40b-425c-8219-7a8f338ac847.PNG)
-----------------------------------------------------------------------------------------
![9](https://user-images.githubusercontent.com/80118008/129153056-0965d5dd-4251-4746-8f2e-f79ec02959fd.PNG)
-----------------------------------------------------------------------------------------
![10](https://user-images.githubusercontent.com/80118008/129153058-1117a2a4-2ef9-4bbc-abf6-84dc4467614c.PNG)
-----------------------------------------------------------------------------------------
![12](https://user-images.githubusercontent.com/80118008/129153060-d115601f-213d-4abe-9246-6ee96e1181f6.PNG)
-----------------------------------------------------------------------------------------
![13](https://user-images.githubusercontent.com/80118008/129153061-9605a58c-726f-4dcc-80d1-57e7836ac757.PNG)
-----------------------------------------------------------------------------------------
![16](https://user-images.githubusercontent.com/80118008/129153062-b58735f3-8e73-40ef-9615-e0cd808ae020.PNG)
-----------------------------------------------------------------------------------------
![18](https://user-images.githubusercontent.com/80118008/129153063-5ecbf1ca-ad12-48de-bf5e-adaca0eafac4.PNG)
-----------------------------------------------------------------------------------------
![20](https://user-images.githubusercontent.com/80118008/129153064-9a8439a7-8854-4417-80af-bfe36f5d64a4.PNG)
-----------------------------------------------------------------------------------------
![21](https://user-images.githubusercontent.com/80118008/129153067-4bc0d63e-5079-406b-9e27-44964420cf5a.PNG)
-----------------------------------------------------------------------------------------
![22](https://user-images.githubusercontent.com/80118008/129153068-e6f05090-017c-4b2d-a260-2cea350a19ea.PNG)
