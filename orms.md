# Object-Relational Mappers (ORMs)

Comparing ActiveRecord in Ruby/Rails with SQLAlchemy in Python

## Creation of Tables - Mapping a Class

### ActiveRecord:
Best quote about ActiveRecord: "Magic is not inherently a bad word"  
(http://api.rubyonrails.org/files/activerecord/README_rdoc.html)  
Automated mapping between classes and tables, attributes and columns.

    class Product < ActiveRecord::Base
    end

The Product class is automatically mapped to the table named "products",
which might look like this:

    CREATE TABLE products (
      id int(11) NOT NULL auto_increment,
      name varchar(255),
      PRIMARY KEY  (id)
    );
    
This would also define the following accessors: `Product#name` and
`Product#name=(new_name)`

### SQLAlchemy: 

SQLAlchemy uses Declarative base (less magic, but still lots going on under the hood [1]).  
You have to explicitly import classes from the SQLAlchemy library (even things like data types!)

http://docs.sqlalchemy.org/en/rel_0_9/orm/extensions/declarative.html

    from sqlalchemy.ext.declarative import declarative_base
    from sqlalchemy import Column, Integer, String
    
    Base = declarative_base()
    class SomeClass(Base):
        __tablename__ = 'some_table'
        id = Column(Integer, primary_key=True)
        name =  Column(String(50))

[1] *Specifically, the creation of a [Table](http://docs.sqlalchemy.org/en/rel_0_9/core/metadata.html#sqlalchemy.schema.Table) and [mapper()](http://docs.sqlalchemy.org/en/rel_0_9/orm/mapper_config.html#sqlalchemy.orm.mapper) object

## Connecting to database

### ActiveRecord:
# connect to SQLite3
ActiveRecord::Base.establish_connection(adapter: 'sqlite3', database: 'dbfile.sqlite3')

    # connect to MySQL with authentication
    ActiveRecord::Base.establish_connection(
        adapter:  'mysql2',
        host:     'localhost',
        username: 'me',
        password: 'secret',
        database: 'activerecord'
    )
    
    
