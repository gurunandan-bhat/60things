# Consolidating, Organizing and Managing Data

## Why Consolidate

 As organizations scale, the data that they use for their work can
 quickly outgrow their original scale in every aspect - size,
 complexity and variety, technology and access control. Data stored in
 small spreadsheets, text based lists and even single-file databases
 becomes critical to success. As use proliferates, so do users, which
 in turn, requires a fine balance of conflicting aspects: making it
 available for wide internal distribution to drive innovation, and,
 protecting its safety and integrity by intelligent access controls.

 Consolidating data is the first step in beginning to address these
 issues. The root of the word consolidate is *con* (combine or bring
 together) and *solidaire* (make firm) - "bringing together to make
 firm", and so the two roots give this exercise two equally important
 aspects - "bringing together" nad "make firm".

 In the context of technology each aspect means:

**Bring Together:** First and most importantly, we must provide a
single UI to users - what, in jargon is an /extensible/, published
Service API that both humans (sometimes) and applications (mostly) can
use to query and discover relations. Second it requires us to do a
complete sweep of all data sources some in plain sight, some hidden in
users personal spreadsheets and lists. While this does automatically
imply the need to store all data in a single location and technology
stack (a database), doing so has profound positive implications for
the second aspect of consolidating, which is;
 
**Make Firm:**: A "firm" Datastore is one that is organized to reflect
a business' activity, and one that scales nicely with time and
success. Be sure that your data will grow exponentially - both in
volume (more users, more content) and in variety (newer products,
newer relationships between products and consumers, newer patterns of
consumption, newer transactions etc.) A simple test of a good data
store is one where every new innovation can be recorded simply as a
new row in some table. An "in-firm" store is one where every new
pattern requires designing a new table or adding a new column in an
already overloaded table. A firm data store requires well defined
access controls that can toggled quickly. A firm data store can be
easily backed up, the back-up tested periodically and restored quickly
after a disaster. All these aspets become hugely easier when we use a
single technology stack for storing, accessing and managing the data
store.

## How might one Consolidate 

Here I will describe one possible progression of steps to our final
goal of a consolidated data store in four steps

1. **Design** a maximally scalable schema for a SQL based relational
   database. The specific product (MySQL, PostgreSQL, Oracle etc.) is
   not important and this schema should work in most enterprise grade
   relational backends. This will require a solid understanding of our
   business and some amount of future-gazing. We will begin with a
   very high-level view of business entities and their relations and
   encode them in tables. There is the possibility of going wrong and
   requiring incremental modifications in the initial period of
   use. But as long as we care careful, these increments will be small
   and hopefully far between. If that is not the case, it means an
   overall re-think is called for.
2. **Import** data into the new schema. This is probably the easiest
   part since much of it can be scripted. If something goes wrong,
   clean up, fix, and redo. It does it have its difficult part and
   that is validation. Since your script does all the heavy lifting,
   its quite dumb (not your fault, really) so imported data can be
   bad. But the clean-up-begin-again solution happens very
   often. There is a critical part to importing, but it will be
   described a bit later when the context is better laid out.
3. **Views** need to be constructed now. Constructing views over raw
   data is very similar to University Campuses constructing pathways -
   look at the area where the grass is worn down and build a path
   along those curves. Those are the paths that people are actually
   using. Building good views involves waiting for a while, examining
   the logs and converting the SQL-Joins that users and applications
   are calling repeatedly and convert the joins into views. Easy. But
   you do need to watch out because time can be your enemy. The trick
   is to examine and review the logs for the right length of
   time. Also most databases now allow *wriatble* views.
4. **Access Control and Roles** is a task to be taken up in parallel
   with constructing roles. Once you have the base tables and views,
   it is a good idea to review logs and find out who (or more often
   *what*) is calling which table and *WHY*! that should guide your
   creation of roles and setting rules for access. Much of the debate
   on access is dominated by concerns of privacy and what suits call
   the "need to know". I believe this is probably a little more
   paranoid than it should be. Better rely on the "need to *use*"
5. **Backup** - needs no justification. But regularly restoring your
   Backup(S) is the DBA's version of eating your own dog food. So we
   need to make sure that this is something that is somebody's most
   important duty (duty, not task). A data store that is not backed up
   at least twice a day and restored less than once a week has zero
   value.

## Design starting from a 5000 ft

From this height, most organizations have just four major data
categories. Of course, to describe items in each category as
completely as possible, you will need many tables, which we will
discover as we descend to ground level carefully. These categories
are:

1. People
2. Assets
3. Relations between People and Assets
4. Real-time Metrics

### People

It is almost always a good idea to keep the People collection/table as
simple as possible, even as bare as a slim addressbook with each
person identified by a unique id (which is not the email, since that
can change). It is fine, even, recommended to keep both internal
employees and external users in a single collection Coupled with a
*Role* master table we can now use a PersonRole combination of primary
identifiers from the Person and Role masters. A new role merely
requires an additional row in the Role master (additional rows are
good, additional columns and tables are generally bad). A quick survey
of the current data will give us a good starting point for populating
the Role master which can be reviewed.

### Assets

This should be a list of every offering you have with every atribute
that is *uniquely* and *permanently* (in the long-term) associated
with it. Identifying these requires a sweep of your assets and an easy
way to start is to list categories of assets (asset type:
e.g. content: possibly further divided into text, audio and video,
merchandize etc.) first and then do a sweep per category. The critical
step here is identifying the unique and long-term attributes of an
asset. We can do a trial list and then sharpen it as we develop.

### People <=> Asset Relations

This a set of tables that will necessarily vary with time rapidly or
slowly depending on how transient the relationship is. Once the People
and Asset tables are identified, identifying relationships becomes
simpler. The most important question to ask when capturing
relationships is this: If this relationship changes, will I have to
add a new column to the table (or modify the schema) or merely create
a new row or update/delete an existing row? A good table design always
leads to merely adding or updating a row, never modifying the table or
the schema.

### Real-time Metrics

This is a whole separate category of tables whose core purpose is
encapsulating Business Intelligence. It is best to usually collect it
in a dynamic TSD (Time-series Database) and then move it to more
static conventional store at some regular interval usually at midnight
of each day. We shall have something to add to this later. For now we
should just leave a task marker to indicate a near-future TODO.

## Reviewing the Current Schema

A good starting point is to review the database created to serve the
mobile app under development and see what modifications might improve
it (if at all):


