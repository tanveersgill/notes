> from Walter Lewin's 8.02x lecture 3

- say you have an electric field, and you introduce an open surface in it
	- that surface has a normal vector
	- we can also take an infinitesemal area of the surface, and call it dA
	- and, it has a local electric field vector E

~~~
^ then, the 'electric flux', denoted dϕ is the dot product:
~~~
$$
dϕ=\vec{E}\cdot\hat{n}dA 
$$
- also, this is a scalar. ( recall dot product of A and B is ABcos(theta) )

- this is just the flux for that tiny area of the surface we chose; we can integrate to calculate the flux through the entire surface
$$
\displaylines
{
\vec{dA}\ is \ the\ same\ as\ \hat{n}dA
\\
both\ are\ perpendicular\ to\ the\ area\ chosen.
}
$$

***some intuition (wth is flux?)***
- **flux** is the process of flowing, whether in or out of something
- nice to compare it to air flow
~~~
say you have a window.
	- it has area A
	- air flows straight thru the window at a velocity v
	- at what rate does air go through the window?
		- v x A
	 ___
	|  -->
	|  -->
	 ---
	- in this case, the air is flowing parallel to the normal of the surface

now, we tilt the window
	____
	\  ---->
	 \  ---->
	  \____
	- the normal is now diagonal and not parallel w/ the air
	- now we have to take the dot product because we care about the flow going in a direction that is not parallel to the normal

what if the window is placed flat?
      -->
	======
	  -->
	- no air goes thru!
~~~
- now, take everything above and replace the window with any surface, and air with an electric field

## with a non-open surface
- above, the normal vector was not really well-defined, due to the surface being open
- if the surface is closed, the normal must always go inside -> out
	- moreover, each point may have a different normal vector direction.

- for such a surface, we can compute the total flux going through it:
	- look at each flux locally for every area dA on the surface, and integrate to find a total
$$
\phi=\oint{\vec{E}\cdot\vec{dA}}
$$
- the circle here just means we're integrating over a closed surface

