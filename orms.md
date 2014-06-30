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

SQLAlchemy uses Declarative base (less magic)
http://docs.sqlalchemy.org/en/rel_0_9/orm/extensions/declarative.html

    from sqlalchemy.ext.declarative import declarative_base
    Base = declarative_base()
    class SomeClass(Base):
        __tablename__ = 'some_table'
        id = Column(Integer, primary_key=True)
        name =  Column(String(50))
