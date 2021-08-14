# Description

I have documented here my two CRUD projects that I made as a class project. At first I learned the fundemental logic of .NET Core and EntityFramework work flows.
the first project,A Console output project which where you can Create a post,Create a comment,Create a user(Menu 8),View,Edit and Delete.and the second project can Create,View and edit columns as a WinForm GUI.

# DataAnnotations
**●DBContext Class**

The Data-Base Context class is connecting to SQL via the OnConfiguring method which contains a DbContextOptionsBuilder object where I can connect into the Data-Base                        
 objectName.UseSqlServer("Server=localhost\\SQLEXPRESS;Database=Data-Base;Trusted_Connection=True;MultipleActiveResultSets=True;");
 
![DataAnnotationContext](https://user-images.githubusercontent.com/80118008/129166374-86b680d9-21c0-491a-800e-a99f6d466dae.PNG)


**●The Classes**

The Posts Class is now being written and I am using here* DataAnnotations method so for example Post_Id will be the PrimaryKey in the Table so I will use [Key] one line above.
After giving each column its type I open up NuGet PMC and add-migration,update-database.

![DataAnnotation](https://user-images.githubusercontent.com/80118008/129145704-fb56d844-1d56-463a-a9d7-128f35469433.PNG)

# FluentAPI 
**●Fluent Classes**

After using Data Annotations I created two new classes both with the same columns and values as in Posts and Comments Class, only now I remove all [annotations].        
The new Class called FluentPostConfig will inherit from IEntityTypeConfiguration interface using .Metadata.Builders
And now I use the Configure method which contains a generic EntityTypeBuilder object and now I can start using the Fluent code,for example like before I want Post_Id to be my PK so I can write now objectName.HasKey(p => p.Post_Id);

![fluentAPI](https://user-images.githubusercontent.com/80118008/129149864-727efbbc-db4d-49f5-8dde-4750aec7f814.PNG)
*the lambada expression will indicate that the Post_Id column is the PrimaryKey of the table.*

**●DBContext Class**

The Data-Base Context class uses the same DataBase Set properties only now I wont be using the OnConfiguring method I will use the OnModelCreating method which contains a ModelBuilder object which will apply configurations to the Data-Base so in the code I am using the FluentConfig classes that I made before because I want to stay as orginaized as I can.

![FAPICONTEXT](https://user-images.githubusercontent.com/80118008/129166862-0bccc0bb-502c-44c8-a048-20bca182b013.PNG)


# Second Project - WinForms CRUD

![0](https://user-images.githubusercontent.com/80118008/129446849-17f4b050-b703-4576-92a5-59eaec44c745.PNG)

![1](https://user-images.githubusercontent.com/80118008/129155592-6a67e2d9-8ff4-4652-bac0-2619f473ee00.PNG)

![2](https://user-images.githubusercontent.com/80118008/129155598-c8baad55-53cf-496f-8bf4-ff1a06eb16c1.PNG)

![3](https://user-images.githubusercontent.com/80118008/129155600-eb0956f2-1d45-49c4-bdc1-4b6ff3396f0b.PNG)

![4](https://user-images.githubusercontent.com/80118008/129155602-7080e842-a995-4ee4-8def-2ff7178cc066.PNG)

![5](https://user-images.githubusercontent.com/80118008/129155604-bdfdcb3f-644f-479c-ac1a-2fb29800440b.png)

![6](https://user-images.githubusercontent.com/80118008/129155605-c9935e72-5ac2-4ccb-9c3b-3f211da630f2.png)

![7](https://user-images.githubusercontent.com/80118008/129155606-2161873e-62b6-4c24-98c1-c030491e46fb.png)

# First Project - Console CRUD

![0](https://user-images.githubusercontent.com/80118008/129153047-22fb2746-8314-462c-9b62-074893aa3f3e.PNG)

![2](https://user-images.githubusercontent.com/80118008/129153049-e288d559-6d50-4cbc-ba5d-0c0c9137cebb.PNG)

![3](https://user-images.githubusercontent.com/80118008/129153051-a4e714df-776d-4092-b603-95d15e7093d2.PNG)

![6](https://user-images.githubusercontent.com/80118008/129153052-2b52ffb8-d898-4f72-ac59-358c0e3274d5.PNG)

![8](https://user-images.githubusercontent.com/80118008/129153055-11791e8d-e40b-425c-8219-7a8f338ac847.PNG)

![9](https://user-images.githubusercontent.com/80118008/129153056-0965d5dd-4251-4746-8f2e-f79ec02959fd.PNG)

![10](https://user-images.githubusercontent.com/80118008/129153058-1117a2a4-2ef9-4bbc-abf6-84dc4467614c.PNG)

![12](https://user-images.githubusercontent.com/80118008/129153060-d115601f-213d-4abe-9246-6ee96e1181f6.PNG)

![13](https://user-images.githubusercontent.com/80118008/129153061-9605a58c-726f-4dcc-80d1-57e7836ac757.PNG)

![16](https://user-images.githubusercontent.com/80118008/129153062-b58735f3-8e73-40ef-9615-e0cd808ae020.PNG)

![18](https://user-images.githubusercontent.com/80118008/129153063-5ecbf1ca-ad12-48de-bf5e-adaca0eafac4.PNG)

![20](https://user-images.githubusercontent.com/80118008/129153064-9a8439a7-8854-4417-80af-bfe36f5d64a4.PNG)

![21](https://user-images.githubusercontent.com/80118008/129153067-4bc0d63e-5079-406b-9e27-44964420cf5a.PNG)

![22](https://user-images.githubusercontent.com/80118008/129153068-e6f05090-017c-4b2d-a260-2cea350a19ea.PNG)
