select sum(users), html_ref, first_url, prev_url, url from 
(select 
      count(distinct(user_id)) AS users,
      first_value(url) over (partition by session_id order by page_number) as first_url,
      lag(url) over (partition by session_id order by page_number) as prev_url,
      url, 
      page_number,
      html_ref
    from traffic 
  where traffic_date >= days_sub(now(), 7)
  and hit_type='PAGE'
  group by url, page_number, session_id, html_ref) AS Summary
where html_ref like '%inline%' 
and prev_url IS NOT NULL
group by html_ref, users, first_url, prev_url, url
order by sum(users) DESC
