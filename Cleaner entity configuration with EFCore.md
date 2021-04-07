Gives an overview of data annotations vs fluent, and a cleaner way of doing entity configuration in EF Core

```
protected override void OnModelCreating(ModelBuilder modelBuilder) {
	base.OnModelCreating(modelBuilder);
	modelBuilder.Entity<SomeEntity>()
		.Property(x => x.MyField).IsRequired();
}
```

Instead of the above, and adding more and more Entities into the OnModelCreating, the blog post advocates for using IEntityTypeConfiguration. 

```
public class MyEntityConfiguration : IEntityTypeConfiguration<MyEntity>
{
	public void Configure(EntityTypeBuilder)<MyEntity> builder) 
	{
		builder.Property(x => x.MyField).IsRequired();
	}
}
```
This allows for splitting the definitions into class specific files

---
https://dotnetcoretutorials.com/2020/06/27/a-cleaner-way-to-do-entity-configuration-with-ef-core/