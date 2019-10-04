# Advice Memo

To: ${ user}

From: Andrew Green

Date: ${ format_date(today())}

We want to quickly review the information we have received from you. You have told us that 
% if Alberta_resident:
you live in Alberta 
% else:
you do not live in Alberta 
% endif
% if location_matter:
and the matter is located in Alberta.
% else:
and the matter is not located in Alberta.
% endif
% if criminal_matter:
You have told us that this is a criminal matter and we can assist with this.
% elif family_matter:
You have told us that this is a family matter and we can assist with this.
% else:
This is neither a family matter nor a criminal matter. Unfortunately, your issue is outside of our mandate.
% endif
% if afford_lawyer:
  You have told us that you can afford to retain a lawyer.
% else:
  You have told us that you are unable to afford a lawyer.
% endif
% if has_lawyer:
  You have told us that you already have a lawyer
% else:
You do not currently have a lawyer.
% endif
% if acting_lawyer:
 and your lawyer is currently acting in this matter.
% endif
% if appeal_matter:
  Because this matter is something that Legal Aid has been previously retained on in the past we will provide as much assistance as possible.
% endif

% if can_help:
We are pleased to inform you that we have determined that you meet our requirements for assistance and we will be able to assist you with this matter.
% else:
We are writing to inform you that you do not meet the requirements of our organization for assistance.
% endif

The following memo attempts to determine if 
% if like_cats:
our good friend 
% else:
evil cat-hater 
% endif
${user.name.first} who was born ${ user.birthdate}.  I wonder if he/she knows he/she was born on a ${format_date( user.birthdate, format='EEEE')}.  That is, he/she was born on ${format_date( user.birthdate, format='full')} 
We know that ${user.name.first} ${user.name.last}
% if like_cats:
likes cats and is therefore a good person and incapable of committing a crime.
% else:
likes dogs and is likely to have committed other horrible crimes.
% endif

% if len(child_household) ==0:
You are childless and life is good.
% elif len(child_household) ==1:
You have one child named: ${child_household}.
% else:
You have more than one child.  The names of your children are: ${child_household}.
% endif
