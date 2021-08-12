# EntityFramework - FluentAPI and DataAnnotations

Two CRUD projects that I made as a class project.At first I started learning the fundemental logic of .NET Core and moved onto the first project.I started writing the code by the right EF work flows, first the Console output project which where you can Create a post,Create a comment,Create a user(Menu 8),Edit and Delete.

**DataAnnotations**
# .DBContext Class

The Data-Base Context class is connecting to SQL via the OnConfiguring method which contains a DbContextOptionsBuilder object where I can connect into the Data-Base
 objectName.UseSqlServer("Server=localhost\\SQLEXPRESS;Database=Data-Base;Trusted_Connection=True;MultipleActiveResultSets=True;");
 ![DataAnnotationContext](https://user-images.githubusercontent.com/80118008/129145644-5800eeb2-d8aa-4334-9cc1-bd0c9fb9dd5b.PNG)

# .The Class's

The Posts Class is now being writing and I am using here* DataAnnotations method so for example Post_Id will be the PrimaryKey in the Table so I will use [Key] one line above.
After giving each column its type I open up NuGet PMC and add-migration,update-database.
![DataAnnotation](https://user-images.githubusercontent.com/80118008/129145704-fb56d844-1d56-463a-a9d7-128f35469433.PNG)

--------------------------------------------------------------
**FluentAPI**
# .Fluent Class's

After using Data Annotations I created two new class's both with the same columns and values as in Posts and Comments class's only now I remove all [annotations].
Now I can create a new Class called FluentPostConfig which will inherit from IEntityTypeConfiguration interface using .Metadata.Builders
And now I use the Configure method which contains a generic EntityTypeBuilder object and now I can start using the Fluent code,for example like before I want Post_Id to be my PK so I can write now objectName.HasKey(p => p.Post_Id);
![fluentAPI](https://user-images.githubusercontent.com/80118008/129149864-727efbbc-db4d-49f5-8dde-4750aec7f814.PNG)
* the lambada expression will indicate that Post_Id column is the PrimaryKey of the table.

# .DBContext Class

The Data-Base Context class uses the same DataBase Set properties only now I wont be using the OnConfiguring method I will use the OnModelCreating method which contains a ModelBuilder object which will apply configurations to the Data-Base so in the code I am using the FluentConfig class's that I made before because I want to stay as orginaized as I can.
![fluentAPIContext](https://user-images.githubusercontent.com/80118008/129150720-41aaeedc-719d-4fb8-9f1e-e1bd9215be26.PNG)

--------------------------------------------------------------

# First Project - Console CRUD

![0](https://user-images.githubusercontent.com/80118008/129146013-41210369-a0ae-4afa-ab35-e5b466d214be.PNG)
--------------------------------------------------------------
![2](https://user-images.githubusercontent.com/80118008/129146015-c0b7c3fb-b6fd-4f3e-bd1d-4e8c94bd644a.PNG)
--------------------------------------------------------------
![3](https://user-images.githubusercontent.com/80118008/129146017-904ba63d-9e1a-40a0-a36e-b9b6d244bd50.PNG)
--------------------------------------------------------------
![6](https://user-images.githubusercontent.com/80118008/129146020-a3bbbc12-676d-44ae-a1ef-9f709fdcb7cd.PNG)
--------------------------------------------------------------
![8](https://user-images.githubusercontent.com/80118008/129146022-41a30358-8cd2-48ae-9082-2df6c6262f58.PNG)
--------------------------------------------------------------
![9](https://user-images.githubusercontent.com/80118008/129146023-4595f323-0193-4a3b-bfbc-2f7abfb96e39.PNG)
--------------------------------------------------------------
![10](https://user-images.githubusercontent.com/80118008/129146024-63262677-1cf4-4045-918f-b2be2ab4bf8f.PNG)
--------------------------------------------------------------
![12](https://user-images.githubusercontent.com/80118008/129146026-98c8b919-6d6f-47f6-a9e2-7d5cbb8299b0.PNG)
--------------------------------------------------------------
![13](https://user-images.githubusercontent.com/80118008/129146027-dd757380-a60b-4279-b385-e2aab14fee3d.PNG)
--------------------------------------------------------------
![16](https://user-images.githubusercontent.com/80118008/129146029-ca04e38c-3810-43bb-b78f-ab98b9c9ad6c.PNG)
--------------------------------------------------------------
![18](https://user-images.githubusercontent.com/80118008/129146030-6c8fc6bf-5240-4f50-93b0-015eaf9e6ff5.PNG)
--------------------------------------------------------------
![20](https://user-images.githubusercontent.com/80118008/129146032-cb3008ff-e395-48e0-8c9d-9e453d65e833.PNG)
--------------------------------------------------------------
![21](https://user-images.githubusercontent.com/80118008/129146033-6f7fb86e-bbac-4dbf-8361-5ceed311c92c.PNG)
--------------------------------------------------------------
![22](https://user-images.githubusercontent.com/80118008/129146036-c97dac7a-ac7f-4ff3-9784-16dbb4b21c40.PNG)

# Second Project - WinForms CRUD (no delete option)

![1](https://user-images.githubusercontent.com/80118008/129148300-8ff56f26-d417-47ab-b41b-932a0e24ed65.PNG)
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
